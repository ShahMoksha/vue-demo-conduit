<template>
  <div>
    <br />
    <h1 class="text-xs-center">Your Settings</h1>

    <b-container class="bv-example-row">
      <b-row>
        <b-col sm="6" offset="3">
          <b-form>
            <b-form-group id="input-group-1">
              <b-form-input id="input-1" type="text" required placeholder="URL of profile picture"></b-form-input>
            </b-form-group>

            <b-form-group id="input-group-2">
              <b-form-input
                id="input-2"
                v-model="formData.aboutArticle"
                type="text"
                required
                placeholder="Your username"
              ></b-form-input>
            </b-form-group>

            <b-form-group>
              <b-form-textarea
                id="textarea"
                placeholder="Short bio about you"
                rows="8"
                max-rows="8"
              ></b-form-textarea>
            </b-form-group>

            <b-form-group id="input-group-3">
              <b-form-input id="input-3" type="email" required placeholder="Email"></b-form-input>
            </b-form-group>

            <b-form-group id="input-group-4">
              <b-form-input id="input-4" type="password" required placeholder="Password"></b-form-input>
            </b-form-group>
            <b-form-group>
              <b-button type="submit" variant="primary" class="article">Update Settings</b-button>
            </b-form-group>
            <hr />
            <b-button
              style="float: left"
              class="btn btn-outline-danger"
              variant="outline-primary"
            >Or click here to logout.</b-button>
          </b-form>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      formData: {
        articleTitle: "",
        aboutArticle: ""
      }
    };
  }
};
</script>


<style scoped>
.article {
  float: right;
  background-color: #449d44;
  border-color: #419641;
}
</style>
