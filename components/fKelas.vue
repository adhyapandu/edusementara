<template>
    <div>
    <b-card-group deck>
    <b-card header="Sekolah Dasar" style="margin:20px">
    <b-list-group horizontal="">
      <b-list-group-item href="#"><nuxt-link class="text-dark" to="/Kumpulan_Soal" >Kelas 1</nuxt-link></b-list-group-item>
      <b-list-group-item href="#">Kelas 2</b-list-group-item>
    </b-list-group>
    <b-list-group horizontal="">
        <b-list-group-item href="#">kelas 3</b-list-group-item>
        <b-list-group-item href="#">kelas 4</b-list-group-item>
    </b-list-group>
    <b-list-group horizontal="">
        <b-list-group-item href="#">kelas 5</b-list-group-item>
        <b-list-group-item href="#">kelas 6</b-list-group-item>
    </b-list-group>
  </b-card>
  <b-card header="Sekolah Menegah Pertama" style="margin:20px">
    <b-list-group>
      <b-list-group-item href="#">Kelas 7</b-list-group-item>
      <b-list-group-item href="#">Kelas 8</b-list-group-item>
      <b-list-group-item href="#">Kelas 9</b-list-group-item>
    </b-list-group>
  </b-card>
</b-card-group>
<b-card-group deck>
    <b-card header="Sekolah Menengah Atas" style="margin:20px">
    <b-list-group>
      <b-list-group-item href="#">Kelas 10</b-list-group-item>
      <b-list-group-item href="#">Kelas 11</b-list-group-item>
      <b-list-group-item href="#">Kelas 12</b-list-group-item>
    </b-list-group>
  </b-card>
  <b-card header="Sekolah Menengah Kejuruan" style="margin:20px">
    <b-list-group>
      <b-list-group-item href="#">Kelas 10</b-list-group-item>
      <b-list-group-item href="#">Kelas 11</b-list-group-item>
      <b-list-group-item href="#">Kelas 12</b-list-group-item>
    </b-list-group>
  </b-card>
  <b-card header="Sekolah Luar Biasa" style="margin:20px">
    <b-list-group horizontal="">
      <b-list-group-item href="#">SLB A</b-list-group-item>
      <b-list-group-item href="#">SLB B</b-list-group-item>
    </b-list-group>
    <b-list-group horizontal="">
        <b-list-group-item href="#">SLB C</b-list-group-item>
        <b-list-group-item href="#">SLB D</b-list-group-item>
    </b-list-group>
    <b-list-group horizontal="">
        <b-list-group-item href="#">SLB E</b-list-group-item>
        <b-list-group-item href="#">SLB F</b-list-group-item>
    </b-list-group>
  
  </b-card>
</b-card-group>
    </div>
</template>

<script>
export default {
    name: 'fKelas',
}
</script>