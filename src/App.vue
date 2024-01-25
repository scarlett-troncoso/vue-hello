<script>
export default {
  name: "App",
  data() {
    return {
      message: 'CIAO A TUTTI ☻',
      image: 'universo.jpg',
      image2: '/pianeta-terra.jpg',
      classeImg: 'sizeImg'
    };
  },

  methods: {
    imagePath: function (img) {
      return new URL(`./assets/${img}`,
        import.meta.url).href;
    }
  }
};
</script>

<template>
  <div>
    <h1>{{ message }}</h1>
  </div>

  <div>
    <img :src="imagePath(image)" v-bind:class="classeImg"> <!--image con data e methods-->
  </div>
  <div>
    <img :src="image2" v-bind:class="classeImg"> <!--image con data e PROVA PER USARE CARTELLA PUBLIC-->
  </div>
</template>


<style></style>
