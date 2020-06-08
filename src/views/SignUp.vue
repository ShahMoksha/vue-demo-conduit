<template>
  <div>
    <h1 class="text-xs-center">Sign up</h1>
    <p class="text-xs-center">
      <a href="/signin" class>Have an account?</a>
    </p>
    <b-container class="bv-example-row">
      <b-row>
        <b-col sm="6" offset="3">
          <b-form>
            <b-form-group id="input-group-1">
              <b-form-input
                id="input-1"
                v-model="formData.email"
                type="text"
                required
                placeholder="User Name"
              ></b-form-input>
            </b-form-group>

            <b-form-group id="input-group-2">
              <b-form-input id="input-2" type="email" required placeholder="Email"></b-form-input>
            </b-form-group>

            <b-form-group id="input-group-3">
              <b-form-input id="input-3" type="password" required placeholder="Password"></b-form-input>
            </b-form-group>
            <b-button type="submit" variant="primary" class="signup">Sign up</b-button>
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
        name: ""
      }
    };
  }
};
</script>


<style scoped>
.signup {
  float: right;
  background-color: #449d44;
  border-color: #419641;
}
</style>