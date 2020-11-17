<template>
    <div style="margin-top:3%;background-color:#F8F8F8 ;padding:2% 10% 20px 10%">
    <p class="sansserif">Features</p>
  <b-card-group>
    <b-card title="Bank Soal" img-src="https://picsum.photos/250/300/?image=24" img-alt="Image" img-top>
      <b-card-text>
        This is a wider card with supporting text below as a natural lead-in to additional content.
        This content is a little bit longer.
      </b-card-text>
      <nuxt-link to="/BankSoal">Learn More >></nuxt-link>
    </b-card>

    <b-card title="Scheduling" img-src="https://picsum.photos/250/300/?image=26" img-alt="Image" img-top style="margin: 0px 2% 0px 2%">
      <b-card-text>
        This card has supporting text below as a natural lead-in to additional content.
      </b-card-text>
      <nuxt-link to="/scheduling">Learn More >></nuxt-link>
    </b-card>

    <b-card title="Tutor Kami" img-src="https://picsum.photos/250/300/?image=21" img-alt="Image" img-top>
      <b-card-text>
        This is a wider card with supporting text below as a natural lead-in to additional content.
        This card has even longer content than the first to show that equal height action.
      </b-card-text>
      <nuxt-link to="/Tutor">Learn More >></nuxt-link>
    </b-card>
  </b-card-group>
</div>
</template>

<script>
export default {
    name: 'Features',
}
</script>

<style>

</style>