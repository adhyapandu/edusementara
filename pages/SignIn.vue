<template>
    <div class="vue-tempalte">
        <form>
            <h3>Sign In</h3>

            <div class="form-group">
                <label>Email address</label>
                <input type="email" class="form-control form-control-lg" />
            </div>

            <div class="form-group">
                <label>Password</label>
                <input type="password" class="form-control form-control-lg" />
            </div>

            <button type="submit" class="btn btn-dark btn-lg btn-block">Sign In</button>

            <p class="forgot-password text-right mt-2 mb-4"><a href="#">Forgot password ?</a></p>
            <p class="text-center"> or </p>
            <b-container class="bv-example-row bv-example-row-flex-cols">
            <b-row align-h="center">
            <nuxt-link to="SignUp"><button class="btn-dark">SignUP</button></nuxt-link>
            <nuxt-link to="/"><button class="btn-dark">Home</button></nuxt-link>
            </b-row>
            </b-container>
        </form>
    </div>
</template>

<script>
    export default {
        data() {
            return {}
        }
    }
</script>

<style>

body{
  background: #ffffff!important;
  min-height: 100vh;
  display: flex;
  font-weight: 400;
}

.vue-tempalte {
  width: 100%;
  height: 100%;
  margin: auto;
  background: #2554FF;
  box-shadow: 0px 14px 80px rgba(34, 35, 58, 0.2);
  padding: 40px 55px 45px 55px;
  border-radius: 15px;
  margin: 50% 0% 50% 150%;
}


</style>