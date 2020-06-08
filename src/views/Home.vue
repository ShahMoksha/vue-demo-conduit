<template>
  <div>
    <b-jumbotron
      class="banner banner-header"
      header="conduit"
      lead="A place to share your knowledge."
    ></b-jumbotron>
    <router-link to="/NewArticle">New Article</router-link>|
    <router-link to="/settings">Settings</router-link>|
    <router-link to="/User">Moksha</router-link>
  </div>
</template>

<script>
export default {
  name: "Home"
  // components: {
  //   HelloWorld
  // }
};
</script>

<style scoped>
.banner {
  background-color: #5cb85c;
  padding: 1rem 2rem;
}
.banner-header {
  color: white;
  font-family: "titillium web", sans-serif;
}
.display-3 {
  font-size: 56px;
  font-family: "titillium web", sans-serif;
  font-weight: 700;
}
</style>