<template>
  <div class="home">
    <SongVoter msg="Opening Music"></SongVoter>
<!--    <OfficeRadio msg="Opening Music"></OfficeRadio>-->
    <img alt="Spring logo" src="../assets/logo.png">
  </div>
</template>

<script>
// @ is an alias to /src
import SongVoter from "@/components/SongVoter.vue";
// import OfficeRadio from "@/components/OfficeRadio.vue";
export default {
  name: 'home',
    components: {
      // OfficeRadio,
      SongVoter,
    }
}
</script>
