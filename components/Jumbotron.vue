<template>
    <div>
  <b-jumbotron bg-variant="info" style="padding:5% 0 10% 0;">
    <template #header>eduOne</template>

    <template #lead>
      <p style="text-align:center; margin:0px 25% 0px 25%">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta, dolor, tempore corrupti illo vitae aut est eos magnam nulla officiis consectetur eaque architecto nihil placeat commodi.
      </p>
    </template>
    <nuxt-link to="/SignIn"><b-button variant="success">SignIn</b-button></nuxt-link>
    <nuxt-link to="/SignUp"><b-button variant="success">SignUP</b-button></nuxt-link>
  </b-jumbotron>
</div>
</template>

<script>
export default {
    name: 'Jumbotron',
}
</script>

<style>

</style>