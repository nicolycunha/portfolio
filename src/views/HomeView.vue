<template>
  <header class="presentation">
    <div class="about-me">
      <p>
        Oi! Eu me chamo <span>Nicoly Cunha </span> e sou desenvolvedora
        full stack.
      </p>

      <a
        class="contact-me"
        href="http://www.linkedin.com/in/nicoly-oliveira-da-cunha/"
        target="_blank"
      >
        <img src="../assets/icons/sms.svg" alt="Ícone SMS" class="icon" />
        <span class="text">Fale comigo</span>
      </a>
    </div>

    <img
      class="developer"
      alt="Front-end Developer"
      src="../assets/images/developer.svg"
    />
  </header>
  <section class="info">
    <div class="experience">
      <p class="years">+ {{ calculateExperience(new Date("2019-08")) }}</p>
      <span> anos de experiência </span>
    </div>
    <div class="job">
      <img
        class="computer"
        src="../assets/images/computer.svg"
        alt="Desenvolvedora front-end"
      />
      <span> Desenvolvedora front-end </span>
    </div>
  </section>
</template>

<script>
export default {
  name: "HomeView",
  data() {
    return {
      yearsExperience: new Date().getYear() - new Date("2019-08").getYear() - 1,
    };
  },
  methods: {
    calculateExperience(date) { 
      var ageDifMs = Date.now() - date;
      var ageDate = new Date(ageDifMs); 
      return Math.abs(ageDate.getUTCFullYear() - 1970);
    }
  }
};
</script>

<style scoped  lang="scss">
.presentation {
  display: flex;
  align-items: flex-start;
  gap: 100px;
  padding-left: 7rem;
  padding-right: 7rem;

  .about-me {
    display: flex;
    justify-content: flex-start;
    align-items: center;
    flex-direction: column;
    gap: 60px;
    margin-top: 1.5rem;

    p {
      color: #dbdbdb;
      font-size: 1.25rem;

      span {
        color: #bd75f5;
      }
    }

    .contact-me {
      background: #581989;
      font-weight: 700;
      border: none;
      color: #f0f0f0;
      border-radius: 8px;
      padding: 0.3rem 1rem;
      cursor: pointer;
      text-decoration: none;
      overflow: hidden;
      display: flex;
      align-items: center;
      gap: 10px;
      transition: 0.2s;

      &:hover {
        box-shadow: 0 0 10px #865ab9, 0 0 25px #0d0015, 0 0 50px #865ab9;
        transition-delay: 0.2s;
        border: 1px solid #d9a9ff;
        background: transparent;
      }

      &:active {
        box-shadow: 0 0 8px #581989, 0 0 8px #0d0015, 0 0 8px #581989;
        transition: 0.1s;
        color: #581989;
        border: 1px solid #581989;
        background: transparent;
      }

      .icon {
        width: 18px;
        height: 18px;
      }
    }
  }

  .developer {
    z-index: 1;
    width: 300px;
    height: 300px;
  }
}

.info {
  background: #1b1e32;
  border-radius: 8px;
  height: 150px;
  margin-top: -80px;
  margin-bottom: 6.25rem;
  display: flex;
  justify-content: space-around;
  align-items: center;
}

.experience,
.job {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.experience {
  .years {
    color: #7c35b4;
    font-size: 3.5rem;
  }
}

.job {
  .computer {
    margin: 12px 0;
    width: 100px;
  }
}
</style>