<template>
  <div class="about">
    <img
      src="../assets/images/dev.jpg"
      alt="Foto de Nicoly Cunha"
      class="my-photo"
    />
    <div class="about-me">
      <p class="text">
        Meu nome é Nicoly Cunha e sou desenvolvedora de software com foco em
        tecnologias web, formada em Gestão de Tecnologia da Informação, o que me
        proporcionou um perfil analítico, comunicativo e organizado. Atualmente
        trabalho como analista de desenvolvimento de sistemas na Muralis
        Tecnologia. Sou apaixonada por obter novos conhecimentos e colocá-los em
        prática, além disso amo música.
      </p>
      <div class="actions">
        <a href="mailto:nicolyoliveiracunha.2001@gmail.com" target="_blank">
          <img
            src="../assets/icons/gmail.svg"
            alt="Entre em contato pelo email"
          />
        </a>

        <a href="https://www.instagram.com/nii.cunha/" target="_blank">
          <img
            src="../assets/icons/instagram.svg"
            alt="Entre em contato pelo instagram"
          />
        </a>

        <a href="http://www.linkedin.com/in/nicoly-oliveira-da-cunha/" target="_blank">
          <img
            src="../assets/icons/linkedin.svg"
            alt="Entre em contato pelo linkedin"
          />
        </a>

        <a href="https://api.whatsapp.com/send?phone=5511946655558" target="_blank">
          <img
            src="../assets/icons/whatsapp.svg"
            alt="Entre em contato pelo whatsapp"
          />
        </a>

        <a href="https://github.com/nicolycunha" target="_blank">
          <img src="../assets/icons/github.svg" alt="Me encontre no github" />
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AboutView",
};
</script>

<style lang="scss" scoped>
.about {
  padding: 0 7rem 4rem;
  display: flex;
  align-items: center;
  gap: 100px;

  .my-photo {
    height: 200px !important;
    width: 200px !important;
    border-radius: 50%;
  }

  .about-me {
    display: flex;
    flex-direction: column;
    gap: 20px;

    .text {
      font-size: 0.875rem;
      line-height: 1.35rem;
    }

    .actions {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 40px;
    }
  }
}
</style>

