<!-- Please remove this file from your project -->
<template>
  <div class="terminal">
    <div class="window">
      
      <h1 v-for="(item, index) in display" :key="index">
        <span v-html="renderLetters(item)"></span>
      </h1>
    </div>
    <div class="overlay" :class="{ 'overlay-active': overlayActive }"></div>
  </div>
</template>

<script>
export default {
  name: 'Boot',
  data:  () => {
      return {
        overlayActive: false,
        display: [],
        sequence: ['...','initiating Boot Sequence', '.', '.', '.','----------------------', '>> ', '>> Base systems: CHECK ','>> ', '>> uplink connection: ready ','>> ', '>> Secure access: online ',]
      }
  },
  methods: {
    boot(){
      for (let i = 0; i < this.sequence.length; i++) {
        const el = this.sequence[i];
        setTimeout(()=> {
          this.display.push(el)
        }, 50+ ((i+1) * 400) )
      }
      this.finaliseBoot( this.sequence.length * 500 )
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
  .window {
    /* height: 500px; */
  }

</style>

<style lang="scss">

// .char:nth-child(3n+0) {
//   animation: char-flash 0.05s ease-in forwards;
// }

// .char:nth-child(4n+1) {
//   text-shadow: 0 0 7px rgba(#ccc, 0.7);
//   animation: char-in 0.1s ease-in-out forwards;
// }
// .char:nth-child(5n+2) {
//   text-shadow: 0 0 32px rgba(#2aff40, 0.9);
//   animation: char-in 0.2s ease-in-out 0.1s;
// }
// .char:nth-child(7n+4) {
//   color: rgba(#2aff40, 0.8);
//   text-shadow: 0 0 4px rgba(#2aff40, 0.5);
//   animation: char-in 0.2s ease-in-out 0s;
// }
// .char:nth-child(11n+8) {
//   color: rgba(#2aff40, 0.8);
//   text-shadow: 0 0 4px rgba(#2aff40, 0.5);
//   animation: char-in 0.05s ease-in-out 0.2s;
// }
// @for $i from 0 to 6 {
//   .char:nth-child(25n+#{3+$i}) {
//     animation: char-1 12s ease-in-out #{-$i*-0.1}s infinite;
//   }
// }


@keyframes char-1 {
  @for $t from 0 through 100 {
    #{$t}% {
      color: rgba(red, calc( random(40) / 100) + 0.6);
      text-shadow: 0 0 #{random(4)+8}px rgba(red, calc(random(40) / 100 + 0.5));
    }
  }
}

.char {
  opacity: 0;
}
@for $a from 0 through 30 {
  .char-#{$a} {
    text-shadow: 0 0 6px rgba(#fafafa, 0.4);
    animation: char-in 0.1s ease-in-out forwards;
    animation-delay: calc(34 * #{$a}ms);
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
    animation: overlay 0.8s ease-in forwards;
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