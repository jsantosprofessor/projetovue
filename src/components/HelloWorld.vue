<template>
  <div class="landing-page">
    <div class="hero">
      <h1>{{ title }}</h1>
      <p>{{ description }}</p>
      <button @click="buyProduct">Comprar Agora</button>
    </div>
    <div class="features">
      <div class="feature" v-for="(feature, index) in features" :key="index">
        <img :src="feature.image" :alt="feature.title">
        <h3>{{ feature.title }}</h3>
        <p>{{ feature.description }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      title: 'Produto de Marketing Digital',
      description: 'Aprenda as melhores estratégias de marketing digital com nosso curso completo.',
      features: [
        {
          title: 'Estratégias Avançadas',
          description: 'Descubra técnicas avançadas para otimizar suas campanhas.',
          image: 'https://via.placeholder.com/150'
        },
        {
          title: 'Ferramentas Essenciais',
          description: 'Conheça as ferramentas indispensáveis para o marketing digital.',
          image: 'https://via.placeholder.com/150'
        },
        {
          title: 'Suporte 24/7',
          description: 'Receba suporte contínuo para todas as suas dúvidas.',
          image: '@/assets/picture.jpg'
        }
      ]
    };
  },
  methods: {
    buyProduct() {
      alert('Produto comprado!');
    }
  }
}
</script>

<style scoped>
.landing-page {
  text-align: center;
  background: url('@/assets/picture.jpg') no-repeat center center fixed;
  background-size: cover;
  color: white;
  padding: 50px 0;
}

.hero {
  animation: fadeIn 2s ease-in-out;
}

.features {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
  margin-top: 50px;
}

.feature {
  background: rgba(0, 0, 0, 0.7);
  padding: 20px;
  margin: 10px;
  border-radius: 10px;
  width: 300px;
  animation: slideIn 1s ease-in-out;
}

.feature img {
  width: 100%;
  border-radius: 10px;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

@keyframes slideIn {
  from {
    transform: translateY(50px);
    opacity: 0;
  }
  to {
    transform: translateY(0);
    opacity: 1;
  }
}
</style>