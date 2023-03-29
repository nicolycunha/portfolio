<template>
  <main class="main">
    <navbar class="navigation">
      <a
        href="http://www.linkedin.com/in/nicoly-oliveira-da-cunha/"
        target="_blank"
        class="logo text-pop-up-top"
        >&lt;Nicoly Cunha&gt;</a
      >

      <ul class="actions">
        <li><a href="#home">Home</a></li>
        <li><a href="#about">Sobre</a></li>
        <li><a href="#experiences">Experiências</a></li>
        <li><a href="#projects">Projetos</a></li>
        <li><a href="#hard-skills">Conhecimentos</a></li>
      </ul>

      <div class="menu-responsive">
        <div class="line1"></div>
        <div class="line2"></div>
        <div class="line3"></div>
      </div>
    </navbar>

    <section class="content">
      <HomeView id="home"></HomeView>
      <AboutView id="about"></AboutView>
      <ProjectsView id="experiences"></ProjectsView>
      <ExperiencesView id="projects"></ExperiencesView>
      <HardSkillsView id="hard-skills"></HardSkillsView>
    </section>

    <footer class="footer">
      <img src="./assets/images/wave.svg" alt="Footer" class="image-footer" />
    </footer>
  </main>
</template>

<script>
import HomeView from "./views/HomeView.vue";
import AboutView from "./views/AboutView.vue";
import ExperiencesView from "./views/ExperiencesView.vue";
import ProjectsView from "./views/ProjectsView.vue";
import HardSkillsView from "./views/HardSkillsView.vue";

export default {
  data() {
    return {
      active: 0,
    };
  },
  components: {
    HomeView,
    AboutView,
    ExperiencesView,
    ProjectsView,
    HardSkillsView,
  },
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@200;400;500;600;700&display=swap");

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #dbdbdb;
  font-family: "Poppins", sans-serif;
}
.main {
  .navigation {
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: fixed;
    top: 0;
    width: 100%;
    background: #0f1122;
    z-index: 2;
    padding: 1rem 6.25rem;

    .logo {
      color: #ffffff;
      font-size: 2rem;
      font-weight: 700;
      text-decoration: none;

      &:hover {
        animation: logo 2s ease 0s 1 normal forwards;
      }

      @keyframes logo {
        0% {
          transform: scale3d(1, 1, 1);
        }

        30% {
          transform: scale3d(1.25, 0.75, 1);
        }

        40% {
          transform: scale3d(0.75, 1.25, 1);
        }

        50% {
          transform: scale3d(1.15, 0.85, 1);
        }

        65% {
          transform: scale3d(0.95, 1.05, 1);
        }

        75% {
          transform: scale3d(1.05, 0.95, 1);
        }

        100% {
          transform: scale3d(1, 1, 1);
        }
      }
    }

    .actions {
      display: flex;
      justify-content: space-evenly;
      align-items: center;
      list-style: none;
      gap: 40px;

      li a {
        text-decoration: none;
        color: #dbdbdb;

        &::after {
          content: "";
          display: block;
          width: 0;
          height: 2px;
          background: linear-gradient(
            90deg,
            rgb(206, 150, 248) 0%,
            rgb(163, 86, 221) 27%,
            rgba(124, 53, 180, 1) 100%
          );
          transition: width 0.2s ease-in;
          border-radius: 2px;
        }

        &:hover::after {
          width: 100%;
        }
      }
    }

    .menu-responsive {
      display: none;
      cursor: pointer;

      div {
        width: 32px;
        height: 2px;
        background: #766f68;
        margin: 8px;
        transition: 0.3s;
      }
    }
  }

  .content {
    padding: 9rem 6.25rem 0;
  }

  .image-footer {
    margin-bottom: -8px;
  }
}
</style>
