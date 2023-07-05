<template>
  <h1>Projetos</h1>

  <section class="projects">
    <CardProject v-for="repo in repositories" :key="repo" :project="repo" />
  </section>
</template>

<script>
import CardProject from "../components/CardProject";
export default {
  name: "ProjectsView",
  data() {
    return {
      repositories: [],
    };
  },
  components: {
    CardProject,
  },
  methods: {
    getRepositories() {
      this.repositories = [
        {
          name: "WhatsApp Web",
          description:
            "Este repositório foi criado com base no vídeo Aprenda VueJS reconstruindo a interface do WhatsApp Web, com o objetivo de desenvolver um portfólio pessoal.",
          url: "https://github.com/nicolycunha/whatsapp-vue",
          url_project: "https://whatsapp-vue.netlify.app",
          img: "images/projects/whatsapp-vue.jpg",
        },
        {
          name: "Previsão do Futuro",
          description:
            "Esse projeto foi criado através dos estudos na maratona explorer na Rocketseat, com o intuito de construir uma aplicação que pudesse prever o futuro através de perguntas realizadas pelo usuário.",
          url: "https://github.com/nicolycunha/future-prediction",
          url_project: "https://nicolycunha.github.io/future-prediction/",
          img: "images/projects/maratona-explorer.jpg",
        },
        {
          name: "Página de links",
          description:
            "Site onde é possível ancorar diversas páginas, ideal para utilizar na bio do Instagram",
          url: "https://github.com/nicolycunha/linked-pages",
          url_project: "https://nicolycunha.github.io/linked-pages/",
          img: "images/projects/linked-pages.jpg",
        },
        {
          name: "Codar",
          description:
            "Este repositório foi criado com o objetivo de me desafiar a partir do conteúdo estudado sobre front-end com os desafios da DevChallenge",
          url: "https://github.com/nicolycunha/codar",
          url_project: "https://nicolycunha.github.io/codar/",
          img: "images/projects/codar.jpg",
        },
        // {
        //   name: "TikTok",
        //   description:
        //     "Este repositório foi criado com base na Jornada Fullstack da EBAC, com o objetivo de desenvolver um portfólio pessoal através de um clone da plataforma Tiktok.",
        //   url: "https://github.com/nicolycunha/tiktok",
        //   url_project: "https://tiktok-reactjs.netlify.app/",
        //   img: "../assets/images/projects/whatsapp-vue.jpg",
        // },
      ];
    },
  },
  created() {
    this.getRepositories();
  },
};
</script>

<style lang="scss" scoped>
.projects {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 20px;
  margin: 32px 0;
}
</style>