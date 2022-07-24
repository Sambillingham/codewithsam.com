<template>
  <div class="box" :style="transformWindow" :class="{ 'active': active, 'folder': folder  }">
    <div class="bar" @mousedown="$emit('mdown', dragStart($event))" @mouseup="$emit('mup', name)" >{{title}}</div>
    <div class="close" @click="$emit('close', name)">x</div>

    <div class="content">
        <slot></slot>
      </div>
  </div>
</template>

<script>

export default {
  name: 'Window',
  props: ['x', 'y', 'name', 'active', 'title', 'folder'],
  data: () =>  {
    return {
    }
  },
  computed: {
    transformWindow () {
      return `left: ${ this.x }px; top: ${ this.y }px;`
    }
  }, 
  methods: {
      dragStart(event) {
          const e = event
          const rect = event.target.getBoundingClientRect();
          const offsetX = event.pageX - rect.left
          const offsetY = event.pageY - rect.top
          return {name: this.name, x: offsetX, y: offsetY}
      }
      
  }
}
</script>

<style scoped lang="scss">


.box {
    position: absolute;
    background: #181b1f;
    border: solid 1px #ccc;
    box-shadow: 8px 10px 3px rgba(11, 11, 11, 0.8);
    min-width: 280px;
    width: 300px;
    display: none;
}  

.box.active {
  display: block;
}
.box.folder {
  width: 600px;

  .content {
    padding: 0;
  }
}

.bar {
  background: #ccc;
  top: 0;
  left: 0;
  width: 100%;
  // text-align: center;
  padding: 0.4rem;
  font-size: 0.75rem;
  color: #000;
  cursor: grab;
}
.close {
  position: absolute;
  top: 0.2rem;
  right: 0.3rem;
  background: #181b1f;
  color: #ccc;
  padding: 0 0.25rem;
  cursor: pointer;
}
.content {
  padding: 1rem 1.5rem;
}

.content p {
  margin: 0;
}
</style>
