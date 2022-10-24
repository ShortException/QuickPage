<template>
  <div class="listRef">
    <div class="refBlock">
      <div class="ref">
        <img src="./img/youtube.png" alt="not found" onclick="window.open('https://youtube.com', '_blank')">
      </div>
    </div>
    <div class="refBlock">
      <div class="ref">
        <img src="./img/twitch.png" alt="not found" onclick="window.open('https://twitch.tv', '_blank')">
      </div>
    </div>
    <div class="refBlock">
      <div class="ref">
        <img src="./img/github.png" alt="not found" onclick="window.open('https://github.com', '_blank')">
      </div>
    </div>
    <div class="refBlock">
      <div class="ref">
        <img src="./img/twitter.png" alt="not found" onclick="window.open('https://twitter.com', '_blank')">
      </div>
    </div>
    <div class="refBlock">
      <div class="ref">
        <img src="./img/discord.png" alt="not found" onclick="window.open('https://discord.com', '_blank')">
      </div>
    </div>
  </div>
</template>

<script>

export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "RefContainer"
}
</script>

<style scoped>
.listRef {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: normal;
  align-content: stretch;
  margin-left: 300px;
  margin-right: 300px;
}

.refBlock {
  display: block;
  flex-grow: 0;
  flex-shrink: 1;
  flex-basis: auto;
  align-self: auto;
  order: 0;
}

.ref {
  position: fixed;
  margin: 20px;
  border: 2px solid #347dfe;
  padding: 10px;
  background-color: #202025;
  border-radius: 20px;
  transition-duration: 0.2s;
}

.ref:hover {
  box-shadow: 10px 10px 5px 0px rgba(0,0,0,0.75);
  -webkit-box-shadow: 10px 10px 5px 0px rgba(0,0,0,0.75);
  -moz-box-shadow: 10px 10px 5px 0px rgba(0,0,0,0.75);
  padding: 3rem;
}

.ref img {
  width: 80px;
  height: 80px;
  border: 1px solid #202025;
  border-radius: 40px;
  background-color: #202025;
}

.ref a {
  text-decoration: none;
}
</style>