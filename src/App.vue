<template>
  <div id="content">
    <div class="spinnerContent">
      <div id="spinner"></div>
    </div>
    <div id="afterSpinner">
      <h1>Willkommen Sir!</h1>
      <div class="refContainer">
        <ref-container></ref-container>
      </div>
    </div>
  </div>
</template>

<script>
import RefContainer from './refs/RefContainer'

export default {
  name: 'App',
  components: {
    // eslint-disable-next-line vue/no-unused-components
    RefContainer
  },
  mounted() {
    setTimeout(function () {
      document.getElementById("spinner").style.display = "none";
      document.getElementById("afterSpinner").style.display = "block";
    }, 1000)
  }
}
</script>

<style>

* {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: white;
  background-color: #27262d;
}

#afterSpinner {
  display: none;
  margin: 100px;
}

.refContainer {
  margin-right: 100px;
  margin-left: 100px;
  margin-top: 100px;
}

h1 {
  color: #347dfe;
  font-size: 3rem;
}

.spinnerContent {
  margin: 0;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

#spinner {
  width: 56px;
  height: 56px;
  border-radius: 50%;
  border: 9px solid #dbdcef;
  border-right-color: #474bff;
  animation: spinner 1s infinite linear;
}

ref-container {
  height: 200px;
  position: relative;
}

@keyframes spinner {
  to {
    transform: rotate(1turn);
  }
}
</style>
