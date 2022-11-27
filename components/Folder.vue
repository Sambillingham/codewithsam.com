<template>
  <div class="content">
      <div class="list">
        <p @click="folder = 'gm' " :class="{ active : folder == 'gm' }">Good Monkeyz NFT</p>
        <p @click="folder = 'blerg'" :class="{ active : folder == 'blerg' }">On-Chain SVG</p>
        <p @click="folder = 'inc'" :class="{ active : folder == 'inc' }">Bldg Blox Inc</p>
        <p @click="folder = 'steem'" :class="{ active : folder == 'steem' }">Steem Blockchain Dev</p>
        <p @click="folder = 'cmd'" :class="{ active : folder == 'cmd' }">Command Control</p>
      </div>
      <div class="view">
            <div v-if="folder === 'gm' ">
                <h2>Merch &amp; PFP Collection</h2>
                <p></p>
                <a href="https://goodmonkeyz.art">https://goodmonkeyz.art</a>
                <p>Solidity, Nuxt/Vue, Ethers.js, Netlify, Supabase</p>
            </div>
            <div v-if="folder === 'blerg' ">
                <h2>On-Chain SVG </h2>
                <p></p>
                <a href="https://github.com/Sambillingham/pixel-grid-svg-renderer">gh.com/sb/pixel-grid-svg-renderer</a>
                <a href="https://github.com/Sambillingham/blerg-v2-mvp">gh.com/sb/blergs-v2-on-chain</a>
                <p>Solidity, Next/React, Rainbow/Ethers.js, Vercel, Supabase</p>
            </div>
            
            <div v-if="folder === 'inc' ">
                <h2>The BLDG BLOX inc</h2>
                <a href="https://twitter.com/bldg_blox">twitter.com/bldg_blox</a>
                <p>Firebase, Nuxt/Vue</p>
            </div>

            <div v-if="folder === 'steem' ">
                <h2>_Steem Blockchain Dapps_</h2>
                <a href="https://github.com/code-with-sam">github.com/code-with-sam</a>
                <p>Steem Blockchain Dev Tools</p>
            </div>

            <div v-if="folder === 'cmd' ">
                <h2>Command Control</h2>
                <a href="http://command-control.sambillingham.com">https://cmd.sb.com</a>
                <p>Node.js, Arduino, MQTT</p>
            </div>
            
      </div>

      
  </div>
</template>

<script>

export default {
  name: 'Folder',
  data: () =>  {
    return {
      folder: 'blerg'
    }
  },

  methods: {
      
  }
}
</script>

<style scoped lang="scss">

.content {
    display: flex;
    flex-wrap: wrap;
}
.list {
    padding: 2rem;
    cursor: pointer;

    p:hover, .active {
      transition: 200ms all; 

      &::before {
        content: '> '
      }
      background: #ccc;
      color: #333;
      font-weight: 600;
    }
}
.view {
    border-left: solid 1px #ccc;
    flex-basis: 50%;
    padding: 2rem;
    flex-grow: 1;
}
.view h2 {
  margin: 0;
  text-transform: uppercase;
  letter-spacing: 1px;
  font-size: 1rem;
  
}
.view a {
  display: inline-block;
  padding: 0.4rem 0 0;
  color: #ccc;
  border-bottom: dotted 1px #ccc;
  text-decoration: none;
}
</style>
