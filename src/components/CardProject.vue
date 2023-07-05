<template>
  <a :href="project.url_project" target="_blank">
    <div class="card">
      <img :src="getImgUrl(project.img)" :alt="project.name" />
      <h3 class="title">{{ project.name }}</h3>
      <p class="description">{{ project.description }}</p>
    </div>
  </a>
</template>

<script>
export default {
  name: "CardProject",
  props: {
    project: Object,
  },
  methods: {
    getImgUrl(pic) {
      return require("../assets/" + pic);
    },
  },
};
</script>

<style>
a {
  text-decoration: none;
  color: #dbdbdb;
}

.card {
  width: 270px;
  text-align: center;
}

.card img {
  border-radius: 8px;
  width: 270px;
}

.description {
  font-size: 12px;
  line-height: 16px;
}
</style>