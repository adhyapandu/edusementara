<template>
    <div class="vue-tempalte">
        <form>
            <h3>Sign Up</h3>

            <div class="form-group">
                <label>Nama Lengkap</label>
                <input type="input" class="form-control form-control-lg" />
            </div>

            <div class="form-group">
                <label>Email address</label>
                <input type="email" class="form-control form-control-lg" />
            </div>

            <div class="form-group">
                <label>Password</label>
                <input type="password" class="form-control form-control-lg" />
            </div>
            <b-form-group id="input-group-3" label="Pendidikan:" >
        <b-form-select
          id="input-1"
          v-model="form.pendidikan"
          :options="pendidikan"
          required
        ></b-form-select>
      </b-form-group>
        <b-form-group id="input-group-2" label="Kelas:" >
        <b-form-select
          id="input-2"
          v-model="form.kelas"
          :options="kelas"
          required
        ></b-form-select>
        </b-form-group>
            <button type="submit" class="btn btn-dark btn-lg btn-block">Sign Up</button>
            <p class="text-center"> or </p>
            <b-container class="bv-example-row bv-example-row-flex-cols">
            <b-row align-h="center">
            <nuxt-link to="SignIn"><button class="btn-dark">SignIn</button></nuxt-link>
            <nuxt-link to="/"><button class="btn-dark">Home</button></nuxt-link>
            </b-row>
            </b-container>
        </form>
    </div>
</template>

<script>
    export default {
        data() {
            return {
        form: {
          pendidikan: null,
          kelas:null
        },
        pendidikan: [{ text: 'Select One', value: null }, 'SD', 'SMP', 'SMA', 'SLB'],
        kelas: [{ text: 'Select One', value: null }, '1', '2', '3']
      }
    },
    }
</script>

<style>
 

.vue-tempalte {
  width: 100%;
  height: 100%;
  margin: auto;
  background: #ffffff;
  box-shadow: 0px 14px 80px rgba(34, 35, 58, 0.2);
  padding: 40px 55px 45px 55px;
  border-radius: 15px;
  margin: 50% 0% 50% 150%;
}


</style>