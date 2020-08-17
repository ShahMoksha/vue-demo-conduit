<template>
  <div id="app" style="overflow: hidden;">
    <div>
      <b-navbar toggleable="lg" type="light" variant="light">
        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav>
            <b-nav-item href="/">
              <div class="conduit">conduit</div>
            </b-nav-item>
          </b-navbar-nav>
          <b-navbar-nav class="ml-auto">
            <b-nav-item>
              <router-link to="/">Home</router-link>
              <!-- <div v-if="check">hello</div> -->
            </b-nav-item>
            <b-nav-item>
              <router-link to="/signin" :articlePage="articlePage">Sign in</router-link>
            </b-nav-item>
            <b-nav-item>
              <router-link to="/signup">Sing up</router-link>
            </b-nav-item>
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
    </div>
    <router-view />
  </div>
</template>

<script>
export default {
  data() {
    return {
      check: false
    };
  },
  mounted() {
    this.articlePage();
  },
  methods: {
    articlePage() {
      this.check = true;
      // console.log(this.check);
      return this.check;
    }
  }
};
</script>

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

.conduit {
  color: #5cb85c;
  font-family: "titillium web", sans-serif;
  font-weight: 800;
  font-size: 24px;
}
</style>
