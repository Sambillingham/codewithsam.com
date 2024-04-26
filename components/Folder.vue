<template>
  <div class="content">
      <div class="list">
        <p @click="folder = 'hex'" :class="{ active : folder == 'hex' }">Hexapod.industries</p>
        <p @click="folder = 'blerg'" :class="{ active : folder == 'blerg' }">Custon SVG Renderer</p>
        <p @click="folder = 'gm' " :class="{ active : folder == 'gm' }">Good Monkeyz</p>
        <p @click="folder = 'trait'" :class="{ active : folder == 'trait' }">Traits. On-Chain (EVM)</p>
        <p @click="folder = 'inc'" :class="{ active : folder == 'inc' }">Bldg Blox Inc</p>
        <p @click="folder = 'steem'" :class="{ active : folder == 'steem' }">Steem Blockchain</p>
        <p @click="folder = 'cmd'" :class="{ active : folder == 'cmd' }">Command Control</p>
      </div>
      <div class="view">
            <div v-if="folder === 'hex' ">
                <h2>Leading R&amp;D into Meshionics</h2>
                <p>A researcher focusing on Holofact production and exploration.</p>
                <a href="https://hexapod.industries">https://hexapod.industries</a>
                <a href="https://meshionics.com">https://meshionics.com</a>
                <a href="https://myth05.net">https://myth05.net</a>
                <span>**may set your computer on fire)**</span>
            </div>

            <div v-if="folder === 'gm' ">
                <h2>Merch &amp; PFP Collection</h2>
                <p>On-chain verifiable burn-to-order limited edition merch. 2k/2k PFP drop with full provenance and custom minting experience</p>
                <p>Solidity, IPFS, Nuxt/Vue, Ethers.js, Netlify, Supabase</p>
                <a href="https://goodmonkeyz.art">https://goodmonkeyz.art</a>
            </div>
            
            <div v-if="folder === 'blerg' ">
                <h2>Custon svg renderer (EVM)</h2>
                <p>Problem - Deploying on-chain assets to eth can be exepensive.</p>
                <p>Solution - Developed a custom 48x48 4colour on-chain SVG renderer.</p>
                <p>Solidity, Next/React, Rainbow/Ethers.js, Vercel, Supabase</p>
                <a href="https://github.com/Sambillingham/pixel-grid-svg-renderer">pixel-grid-svg-renderer</a>
            </div>
            
            <div v-if="folder === 'trait' ">
              <h2>On-chain Swapable Trait EVM NFTs</h2>
              <a href="https://www.notion.so/Traits-Whitepaper-c5f81db5a9b84c73ad2e89c2697eb77b">Whitepaper</a>
              <p>- Developed a proof of concept for the Blergs DAO</p>
              <a href="https://github.com/Sambillingham/blerg-v2-mvp">https://gh.com/sb/blerg-v2-mvp</a>
              <p>Solidity/EVM</p>
            </div>
            
            <div v-if="folder === 'inc' ">
                <h2>The BLDG BLOX inc</h2>
                <p>Neighborhood collaboration platform. Bringing stakeholders together for good. <p>
                <p>Founding Engineer - Firebase (Realtime Database). Nuxt.js x Serverless/Firebase Backend</p>

                <a href="https://twitter.com/bldg_blox">@bldg_blox</a>
            </div>

            <div v-if="folder === 'steem' ">
                <h2>_Steem Blockchain_</h2>
                <p>Building for the STEEM Proof-of-Brain distribution mechanics.</p>
                <a href="https://github.com/code-with-sam/finallycomments">Finally Comments </a>
                <p>- Disqus comments system with STEEM backend </p>
                <a href="https://github.com/code-with-sam/finallynetwork">Finally Network</a>
                <p> - Blog Engine with STEEM backend</p>
            </div>

            <div v-if="folder === 'cmd' ">
                <h2>Command Control</h2>
                <p>AN INTERACTIVE PHYSICAL COMPUTING GAME <p>
                <p>Node.js, Arduino, MQTT, Websockets</p>
                <a href="http://command-control.sambillingham.com" target="_blank">https://cmd.sb.com</a>
            </div>
            
      </div>

      
  </div>
</template>

<script>

export default {
  name: 'Folder',
  data: () =>  {
    return {
      folder: 'hex'
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
