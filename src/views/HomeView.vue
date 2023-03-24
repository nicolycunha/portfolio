<template>
  <div class="home">
    <div class="presentation">
      <p class="me">
        Oi! Eu me chamo <span>Nicoly Cunha </span> e sou desenvolvedora
        front-end.
      </p>
      <button class="contact-me">Me contate</button>
    </div>

    <img
      class="developer"
      alt="Front-end Developer"
      src="../assets/frontend-developer.svg"
    />
  </div>
  <div class="info-section">
    <div class="experience">
      <p class="years">+ {{ yearsExperience }}</p>
      <span> anos de experiência </span>
    </div>
    <div class="job">
      <img
        class="computer"
        src="../assets/computer.svg"
        alt="Desenvolvedora front-end"
      />
      <span> Desenvolvedora front-end </span>
    </div>
  </div>
</template>

<script>
export default {
  name: "HomeView",
  data() {
    return {
      yearsExperience: new Date().getYear() - new Date("2019-08").getYear() - 1,
    };
  },
};
</script>

<style scoped  lang="scss">
.home {
  display: flex;
  padding: 5rem 10rem;
}

.presentation {
  display: flex;
  justify-content: flex-start;
  align-items: center;
  flex-direction: column;
  gap: 60px;
}

.me {
  color: #dbdbdb;
  font-size: 1.75rem;

  span {
    color: #ffbe18;
  }
}

.contact-me {
  border: none;
  background: #ffbe18;
  color: #1b1e32;
  padding: 0.375rem 1.25rem;
  font-size: 1.25rem;
  border-radius: 4px;
  opacity: 0.9;
  cursor: pointer;

  &:hover {
    opacity: 1;
  }
}

.developer {
  z-index: 1;
}

.info-section {
  background: #1b1e32;
  border-radius: 8px;
  height: 200px;
  width: 90%;
  margin: -145px auto 1rem;
  display: flex;
  justify-content: space-around;
  align-items: center;
}

.experience,
.job {
  display: flex;
  flex-direction: column;

  .years {
    color: #ffbe18;
    font-size: 4rem;
  }

  span {
    color: #ffffff;
  }
}

.job {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.computer {
  margin: 12px 0;
}
</style>