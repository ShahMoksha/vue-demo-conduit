<template>
  <div>
    <h1 class="text-xs-center">Sign in</h1>
    <p class="text-xs-center">
      <a href="/signup" class>Need an account?</a>
    </p>
    <b-container class="bv-example-row">
      <b-row>
        <b-col sm="6" offset="3">
          <b-form>
            <b-form-group id="input-group-1">
              <b-form-input
                id="input-1"
                v-model="formData.email"
                type="email"
                required
                placeholder="Email"
              ></b-form-input>
              value: {{formData.email}}
            </b-form-group>

            <b-form-group id="input-group-2">
              <b-form-input
                id="input-2"
                v-model="formData.password"
                type="password"
                required
                placeholder="Password"
              ></b-form-input>
            </b-form-group>
            <b-button :click="signInButton" type="submit" variant="primary" class="signin">Sign in</b-button>
          </b-form>
          <div v-if="signInButtonCheck">helllllllllllllloooooo</div>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
export default {
  props: {
    articlePage: Function
  },
  data() {
    return {
      formData: {
        email: "",
        password: ""
      },
      signInButtonCheck: false
    };
  },
  mounted() {
    // console.log(this.articlePage);
  },
  methods: {
    signInButton() {
      // console.log("1111111111");
      if (
        this.formData.email === "abc@abc.com" &&
        this.formData.password == "123456"
      ) {
        this.signInButtonCheck = true;
        // console.log(this.signInButtonCheck);
        return this.signInButtonCheck;
      }
      this.articlePage(this.signInButtonCheck);
    }
  }
};
</script>

<style scoped>
.signin {
  float: right;
  background-color: #449d44;
  border-color: #419641;
}
</style>
