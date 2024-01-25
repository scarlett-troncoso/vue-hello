<script>
export default {
  name: "App",
  data() {
    return {
      message: 'CIAO A TUTTI ☻',
      image: 'universo.jpg',
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
    <img :src="imagePath(image)" alt="" v-bind:class="classeImg">
  </div>
</template>


<style></style>
