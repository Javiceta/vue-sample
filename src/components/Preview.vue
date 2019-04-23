<template>
  <div class="preview">
    <h2>{{ title }}</h2>
    <img v-show="image" :src="image" :alt="title">
    <a :href="url">{{ url }}</a>
  </div>
</template>

<script>
export default {
  name: "FwPreview",
  data() {
    return {
      title: "",
      image: "",
      url: ""
    };
  },
  methods: {
    setElement(e) {
      this.name = e.name;
      this.image = e.image;
      this.url = e.url;
    }
  }
};
</script>

<style lang="postcss" scoped>
.preview {
  border: 3px solid #fff;
  width: 300px;
  height: 300px;
  display: flex;
  flex-wrap: wrap;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>
