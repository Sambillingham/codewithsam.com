<template>
  <div class="terminal">
    <div class="window">
      
      <h1 v-for="(item, index) in display" :key="index">
        <span v-html="renderLetters(item)"></span>
      </h1>
    </div>
    <div class="overlay" :class="{ 'overlay-active': overlayActive }"></div>
    <div class="overlay overlay--blue" :class="{ 'overlay-active--blue': overlayActive }"></div>
  </div>
</template>

<script>
export default {
  name: 'Boot',
  data:  () => {
      return {
        overlayActive: false,
        display: [],
        sequence: ['...','SB OS BOOT 0.0.ADVNTR.SRVICE', '.', '.', '.','----------------------', '>> ', '>> Base systems: CHECK ','>> ', '>> uplink connection: ready ','>> ', '>> Secure access: online ', '>> ']
      }
  },
  methods: {
    boot(){
      for (let i = 0; i < this.sequence.length; i++) {
        const el = this.sequence[i];
        setTimeout(()=> {
          this.display.push(el)
        }, 30+ ((i+1) * 250) )
      }
      this.finaliseBoot( this.sequence.length * 300 )
    },
    renderLetters(string) {
      let res = ''
      console.log(string);
      string.split('').forEach( (l,i) => res = res + `<span class="char char-${i}">${l}</span>`)
      console.log(res)
      return res;
    },
    finaliseBoot(delay){
      setTimeout( () => {
        this.overlayActive = true
        setTimeout( () => this.$nuxt.$emit('booted'), 940 )
      }, delay)
    }
  },
  created() {
    this.boot();
  },
}
</script>

<style scoped lang="scss">
  .terminal {
    min-height: 100vh;
    background: #151414;
    color: #9dadad;
    display: flex;
    font-family: 'uni 05_53', 'Courier New', Courier, monospace;
    padding: 5vh 0 0 5vw;
  }

  h1 {
    font-size: 1rem !important;
    margin: 0.1rem 0;
    text-transform: uppercase;
    letter-spacing: 0.02rem;
  }


</style>

<style lang="scss">


.char {
  opacity: 0;
}
@for $a from 0 through 30 {
  .char-#{$a} {
    text-shadow: 0 0 6px rgba(#fafafa, 0.4);
    animation: char-in 0.1s ease-in-out forwards;
    animation-delay: calc(20 * #{$a}ms);
  }
}

@keyframes char-in {
  0% {opacity: 0;} 
  100% {opacity: 1;}
}


  .overlay {
    position: absolute;
    height: 110vh;
    width: 110vw;
    top: -5vh;
    left: -5vw;
    backdrop-filter: blur(3px);
    opacity: 0;
  }
  
  .overlay-active {
    animation: overlay 300ms 100ms ease-in forwards;
  }
  .overlay--blue {
    background: darkblue;
    backdrop-filter: none;
  }
  
  .overlay-active--blue {
    animation: flash 10ms 800ms forwards;
  }

  @keyframes flash {
    100% {
      opacity: 1;
    }
  }
  @keyframes overlay {
    0% {
      opacity: 0;
    }
    20% {
      opacity: 1;
      backdrop-filter: blur(1px);
    }
    40% {
      opacity: 1;
      backdrop-filter: blur(2px);
    }
    60% {
      opacity: 1;
      backdrop-filter: blur(3px);
    }
    80% {
      opacity: 1;
      backdrop-filter: blur(2px);
    }
    100% {
      opacity: 1;
      backdrop-filter: blur(4px);
    }
  }

</style>