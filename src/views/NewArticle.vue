<template>
  <div>
    <br />
    <b-container class="bv-example-row">
      <b-row>
        <b-col sm="9" offset="2">
          <b-form>
            <b-form-group id="input-group-1">
              <b-form-input id="input-1" type="text" required placeholder="Article Title"></b-form-input>
            </b-form-group>

            <b-form-group id="input-group-2">
              <b-form-input
                id="input-2"
                v-model="formData.aboutArticle"
                type="text"
                required
                placeholder="What's this article about?"
              ></b-form-input>
            </b-form-group>

            <b-form-group>
              <b-form-textarea
                id="textarea"
                v-model="formData.text"
                placeholder="Write your article (in markdown)"
                rows="8"
                max-rows="8"
              ></b-form-textarea>
            </b-form-group>

            <b-form-group id="input-group-3">
              <b-form-input
                id="input-3"
                v-model="formData.aboutArticle"
                type="text"
                required
                placeholder="Enter Tags"
              ></b-form-input>
            </b-form-group>

            <b-button type="submit" variant="primary" class="article">Publish Article</b-button>
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
        aboutArticle: "",
        text:""
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
