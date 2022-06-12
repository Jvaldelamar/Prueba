<template>
<div>
  <pagina-view>

    <h1>
Bienvenidos a este sorteo
    </h1>

<v-img class="rifa" src="../assets/rifa.jpg"></v-img>




</pagina-view>
</div>

</template>
<style>
.rifa{
    width: 950px;
    display: block;
    margin: 500 auto 0;
}

</style>
<script>
import PaginaView from "@/views/PaginaView.vue";

export default {
  name: 'contenidos',

  components: {
    PaginaView
}

}

</script>