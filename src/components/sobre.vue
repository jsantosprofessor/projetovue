<template>
    <div class="sobre">
      <transition name="fade">
        <div v-if="showContent" class="content">
          <img src="@/assets/marketing-digital.png" alt="Marketing Digital" class="image" />
          <h1>Marketing Digital</h1>
          <p>Nosso produto de marketing digital oferece soluções inovadoras para aumentar a visibilidade online e atrair mais clientes para o seu negócio.</p>
        </div>
      </transition>
    </div>
  </template>
  
  <script>
  export default {
    name: "SobreComponent",
    data() {
      return {
        showContent: false
      };
    },
    mounted() {
      this.showContent = true;
    }
  };
  </script>
  
  <style scoped>
  .sobre {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #f5f5f5;
  }
  
  .content {
    text-align: center;
    max-width: 600px;
    padding: 20px;
    background: white;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    border-radius: 10px;
  }
  
  .image {
    width: 100%;
    height: auto;
    border-radius: 10px;
    margin-bottom: 20px;
  }
  
  h1 {
    font-size: 2em;
    margin-bottom: 10px;
  }
  
  p {
    font-size: 1.2em;
    color: #555;
  }
  
  .fade-enter-active, .fade-leave-active {
    transition: opacity 1s;
  }
  
  .fade-enter, .fade-leave-to /* .fade-leave-active in <2.1.8 */ {
    opacity: 0;
  }

</style>