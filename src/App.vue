<template>
  <div id="app">
    <div class="mx-auto" style="height: 100vh">
      <div
        class="sidebar float-left border-r"
        style="height: 100vh; width: 300px"
      >
        <h4>Components</h4>
        <ol>
          <li><router-link to="/">Home</router-link></li>
          <li>
            <router-link to="/about">About</router-link>
          </li>
          <li>
            <router-link to="/button">Button</router-link>
          </li>
        </ol>
      </div>
      <div class="float-left p-5" style="height: 100vh">
        <router-view />
      </div>
    </div>
  </div>
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
