<template>
  <div class="main" @mousemove="move($event)">
    <div class="bar bar--top">
      <span class="icon">
        <svg xmlns="http://www.w3.org/2000/svg" width="13" height="13" viewBox="0 0 24 24"><path fill="#222222" d="M12 0c-6.627 0-12 5.373-12 12s5.373 12 12 12 12-5.373 12-12-5.373-12-12-12zm1 16.057v-3.057h2.994c-.059 1.143-.212 2.24-.456 3.279-.823-.12-1.674-.188-2.538-.222zm1.957 2.162c-.499 1.33-1.159 2.497-1.957 3.456v-3.62c.666.028 1.319.081 1.957.164zm-1.957-7.219v-3.015c.868-.034 1.721-.103 2.548-.224.238 1.027.389 2.111.446 3.239h-2.994zm0-5.014v-3.661c.806.969 1.471 2.15 1.971 3.496-.642.084-1.3.137-1.971.165zm2.703-3.267c1.237.496 2.354 1.228 3.29 2.146-.642.234-1.311.442-2.019.607-.344-.992-.775-1.91-1.271-2.753zm-7.241 13.56c-.244-1.039-.398-2.136-.456-3.279h2.994v3.057c-.865.034-1.714.102-2.538.222zm2.538 1.776v3.62c-.798-.959-1.458-2.126-1.957-3.456.638-.083 1.291-.136 1.957-.164zm-2.994-7.055c.057-1.128.207-2.212.446-3.239.827.121 1.68.19 2.548.224v3.015h-2.994zm1.024-5.179c.5-1.346 1.165-2.527 1.97-3.496v3.661c-.671-.028-1.329-.081-1.97-.165zm-2.005-.35c-.708-.165-1.377-.373-2.018-.607.937-.918 2.053-1.65 3.29-2.146-.496.844-.927 1.762-1.272 2.753zm-.549 1.918c-.264 1.151-.434 2.36-.492 3.611h-3.933c.165-1.658.739-3.197 1.617-4.518.88.361 1.816.67 2.808.907zm.009 9.262c-.988.236-1.92.542-2.797.9-.89-1.328-1.471-2.879-1.637-4.551h3.934c.058 1.265.231 2.488.5 3.651zm.553 1.917c.342.976.768 1.881 1.257 2.712-1.223-.49-2.326-1.211-3.256-2.115.636-.229 1.299-.435 1.999-.597zm9.924 0c.7.163 1.362.367 1.999.597-.931.903-2.034 1.625-3.257 2.116.489-.832.915-1.737 1.258-2.713zm.553-1.917c.27-1.163.442-2.386.501-3.651h3.934c-.167 1.672-.748 3.223-1.638 4.551-.877-.358-1.81-.664-2.797-.9zm.501-5.651c-.058-1.251-.229-2.46-.492-3.611.992-.237 1.929-.546 2.809-.907.877 1.321 1.451 2.86 1.616 4.518h-3.933z"></path></svg>
        <span class="title">HEXAPOD //INC distro x.z.0.412</span>
        </span>
        <span class="title">** [SAM][BILLINGHAM] ** </span>
    </div>
    <div class="bar">
        <span class="title">NODE >> N71 >> 0x00</span>
        <!-- <span class="title">** [SAM][BILLINGHAM] ** </span> -->
    </div>
    <section class="group">
    <!-- <div class="window">
      <div class="ascii">

░██████╗░░░██████╗░
██╔════╝░░░██╔══██╗
╚█████╗░░░░██████╦╝
░╚═══██╗░░░██╔══██╗
██████╔╝██╗██████╦╝
╚═════╝░╚═╝╚═════╝░
</div>
    </div> -->
    <!-- <div class="window">
      <div class="social">
        <a href="">
          <svg role="img" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" fill="#ccc"><title>GitHub</title><path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/></svg>
        </a>
        <a href="">
          <svg class="twitter" x="0px" y="0px" viewBox="0 0 100 125" enable-background="new 0 0 100 100">
            <path fill="#ccc" d="M41.2,75.8c-11.7,0-21.2-5.6-21.4-5.7c-0.9-0.6-1.3-1.7-1-2.7c0.4-1,1.4-1.6,2.4-1.5c6.3,0.8,10.7-1.1,13.1-2.7
	c-5.9-4.4-19-17-10.9-35.5c0.3-0.8,1.1-1.3,1.9-1.4c0.8-0.1,1.6,0.3,2.1,1c0.2,0.4,5.9,8.9,20,10.6c0-7.7,6.3-13.9,14-13.9
	c3.4,0,6.7,1.2,9.2,3.5c3.7-0.4,6.6-0.5,6.7-0.5c0.3,0,0.6,0,0.9,0.1c0.5-0.2,1.1-0.2,1.6,0c1.2,0.4,1.7,1.7,1.3,2.9
	c-0.4,1.1-2.5,6.4-5.3,9c0.7,6.5-0.9,16-11.3,26.7C57.1,73.5,48.7,75.8,41.2,75.8z"/>
          </svg>
        </a>
        <a href="">
          
        <svg class="instagram" viewBox="0 0 100 125" x="0px" y="0px">
            <circle fill="none" stroke="#fff" class="cls-1" cx="50" cy="50" r="18.94"/>
            <circle fill="none" stroke="#fff" class="cls-2" cx="74.5" cy="27.13" r="2.91"/>
            <rect fill="none" stroke="#fff" class="cls-1" x="9" y="9" width="82" height="82" rx="19" ry="19"/>
          </svg>
        </a>
        <a href="">██</a>
      </div>    
    </div>  -->
    <!-- <div class="window">
      <div class="data">
        <div>2,400m</div>
        <div>5days</div>
        <div>0.444W 63.000N</div>
        <div>6:42am </div>
      </div>      
    </div> -->
    </section>
    <!-- <section class="group">
        <div class="window window--text">
          Sam Billingham. Full-Stack Developer. Making things with code &amp; cameras. Moved to Norway in 2020 after meeting some Arctic surfers.
        </div>
    </section> -->
    
    <Window name="help" :active="windows.help.active" @mdown="mdown" @mup="mup" @close="closeWindow" :x="windows.help.x" :y="windows.help.y" :title="windows.help.title">
      <p>Sam Billingham. Full-Stack Developer. Making things with code & cameras. You can find me surfing the web || waves. Moved to Norway in 2020 after meeting some Arctic surfers.</p>
    </Window>
    <Window name="weblinks" 
      :active="windows.weblinks.active" 
      @mdown="mdown" @mup="mup" 
      @close="closeWindow" 
      :x="windows.weblinks.x" 
      :y="windows.weblinks.y"
      :title="windows.weblinks.title"
    >
    
      <p><a href="https://github.com/sambillingham">github.com/sambillingham</a> </p>
      <p><a href="https://twitter.com/sam_billingham">twitter.com/sam_billingham</a></p>
      <p><a href="https://www.linkedin.com/in/sambillingham/">linkedin.com/sambillingham</a></p>
      <p><a href="https://www.youtube.com/channel/UCQbOitfNmOUGNqc-uYSJlfw">youtube.com/c/sb</a></p>
      
      
    </Window>

    <Window name="globe" 
      :active="windows.globe.active" 
      @mdown="mdown" @mup="mup" 
      @close="closeWindow" 
      :x="windows.globe.x" 
      :y="windows.globe.y"
      :title="windows.globe.title"
    >
    <globe></globe>
      
    </Window>
    
    <Window name="projects" 
      :active="windows.projects.active" 
      @mdown="mdown" @mup="mup" 
      @close="closeWindow" 
      :x="windows.projects.x" 
      :y="windows.projects.y"
      :title="windows.projects.title"
      :folder="true"
    >
      <Folder/>
      
    </Window>


    <section class="icons">
      <div class="icon"  @click="openWindow('projects')" >
        <img :src="projectIcon" />
        <h2>projects</h2>
      </div>
      <!-- <div class="icon"  @click="openWindow('videos')" >
        <img :src="videoIcon" />
        <h2>videos</h2>
      </div> -->
         <div class="icon"  @click="openWindow('weblinks')" >
        <img :src="linksIcon"  class=""/>
        <h2>weblinks.txt</h2>
      </div>
      <div class="icon"  @click="openWindow('help')" >
        <img :src="aboutIcon"  class="img--32"/>
        <h2>about.txt</h2>
      </div>
 
    </section>
    <div class="bg"></div>
  </div>
</template>

<script>
import Window from '~/components/Window.vue';
import Folder from '~/components/Folder.vue';
import Globe from '~/components/Globe.vue';

import projectIcon from '~/assets/img/projects.png';
import aboutIcon from '~/assets/img/about.png';
import videoIcon from '~/assets/img/videos.png';
import linksIcon from '~/assets/img/links.png';


export default {
  name: 'Interface',
  data:  () => {
      return {
        projectIcon, videoIcon, aboutIcon, linksIcon,
        activeWindow: null,
        windows: {
          globe: {
            active: true,
            offsetX: 0,
            offsetY: 0,
            x: 1090,
            y: 43,
            title: 'Hexapod.industries'
          },
          help: {
            active: true,
            offsetX: 0,
            offsetY: 0,
            x: 200,
            y: 200,
            title: 'About.txt'
          },
          weblinks: {
            active: true,
            offsetX: 0,
            offsetY: 0,
            x: 600,
            y: 300,
            title: 'Weblinks.txt'
          },
          projects: {
            active: false,
            offsetX: 0,
            offsetY: 0,
            x: 400,
            y: 100,
            title: 'Projects'
          },
        }
      }
  },
  components: {
    Window,
    Folder,
    Globe,
  },
  methods: {
    mdown(data) {
      this.windows[data.name].offsetX = data.x
      this.windows[data.name].offsetY = data.y
      this.activeWindow = data.name;
    },
    mup(){
      this.activeWindow = null;
    },
    move(event){
      if(this.activeWindow != null) {
        this.windows[this.activeWindow].x = event.pageX - this.windows[this.activeWindow].offsetX
        this.windows[this.activeWindow].y = event.pageY - this.windows[this.activeWindow].offsetY
      } 
    },
    dragStart() {
      return false;
    },
    openWindow(window) {
      this.windows[window].active = true;
    },
    closeWindow(window){
      this.windows[window].active = false;
    },
    rand(min, max) {
      return Math.floor( Math.random * max ) + min
    }
  },
  created() {

  },
}
</script>

<style scoped lang="scss">
  .main {
    background: #181b1f;
    min-height: 100vh;
    color: #9dadad;
    display: flex;
    overflow: hidden;
    max-height: 100vh;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    position: relative;
  }
  .bar {
    position: fixed;
      bottom: 0;
      width: 100%;
      background: #ccc;
      font-size: 10px;
      padding: 5px 10px;
      font-family: source-code-pro, Menlo, Monaco, Consolas, 'Courier New',
      monospace;
      justify-content: space-between;
      display: flex;
      box-sizing: border-box;
  }
  .bar--top {
    bottom: auto;
    top: 0;
    }

    .icon {
      text-transform: uppercase;
      display: flex;
      align-items: center;
    }
    .icon svg {
        margin-right: 5px;
    }
    .icon .title {
      font-size: 8px;
      // transform: translateY(1px);
      color: #000;
    }
    .bg {
      pointer-events: none;
      position: absolute;
      top: 0;
      left: 0;
      width: 100vw;
      height: 200vh;
      background: repeating-linear-gradient(rgba(47, 163, 170,0.5), transparent 4px, rgba(0, 0, 0, 0.238) 3px, rgba(61, 61, 61, 0.478) 3px);
      mix-blend-mode: color-dodge;
      animation: flicker 2.3s infinite forwards, move 40s infinite alternate;
    }

    @keyframes flicker {
      @for $a from 0 through 100 {
        #{$a}% {
          opacity: calc(calc(random(10) / 100) + 0.5);
        }
      } 
    }
    @keyframes move {
      from {
        transform: translateY(-100vh);
      }
      to {
        transform: translateY(0vh);
      }
    }
    .group {
      display: flex;
      flex-direction: row;
      margin-top: 30vh
    }
    .window {
      background-color: #17191b;
      border: solid #ccc 1px;
      margin: 6px;
      display: flex;
      justify-content: space-between;
      box-shadow: 8px 10px 3px #111;
      padding: 1rem;
    }
    .window--text {
      max-width: 300px;
    }
    .ascii {
      max-width: 160px;
      min-width: 160px;
      margin: 0 auto;
      font-family: monospace;
      color: #ccc;
    }
    .social {
      display: flex;
      flex-direction: column;
    }
    .social a {
      text-decoration: none;
      color: #ccc;
    }

    .icons {
      width: 100%;
      display: flex;
      justify-content: center;
      margin-top: auto;
      margin-bottom: 3rem;
      align-items: baseline;
    }
    .icons .icon {
      text-transform: none;
      display: flex;
      align-items: center; 
      flex-direction: column;
      cursor: pointer; 
      margin: 0 1.2rem;
    }
    .icons img {
      filter: grayscale(100%) contrast(70%);
      // width: 48px;
    }
    .icons .img--32 {
      padding: 5px;
      width: 48px;
    }
    .icons h2{
      font-size: 0.75rem;
    }
</style>
