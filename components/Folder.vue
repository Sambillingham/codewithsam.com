<template>
  <div class="content">
      <div class="list">
        <p>Good Monkeyz</p>
        <p>Bldg Blox Inc</p>
        <p>Steem Blockchain</p>
      </div>
      <div class="view">
            <img src="http://placehold.it/400x400">
            <div>
                Merch Drop &amp; PFP Collection

                Desc: 
                Link: 
                Stack: Solidity, Ethers.js, Nuxt/Vue, Netlify, Supabase,
            </div>
      </div>
        <div class="view">
            <img src="http://placehold.it/400x400">
            <div>
                BLDG Blox Inc - The Building App

                Stack: Solidity, Ethers.js, Nuxt/Vue, Netlify, Supabase,
            </div>
      </div>
      
  </div>
</template>

<script>

export default {
  name: 'Folder',
  data: () =>  {
    return {
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
}
.view {
    border-left: solid 1px #ccc;
    flex-basis: 50%;
    padding: 2rem;
}

</style>
