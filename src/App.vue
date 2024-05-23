<template>
  <div>
    <Navbar />
    <div class="container mt-4">
      <Carousel />
      <div class="card-container mt-4">
        <Card 
          v-for="product in products" 
          :key="product.id" 
          :title="product.name" 
          :description="product.description" 
          :url="product.url" 
        />
      </div>
    </div>
    <Footer />
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue';
import Carousel from './components/Carousel.vue';
import Card from './components/Card.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    Carousel,
    Card,
    Footer
  },
  data() {
    return {
      products: [
        { 
          id: 1, 
          name: 'HEXOHM V3 BLACK ', 
          description: 'Price 3.0000.000', 
          url: 'https://i.pinimg.com/736x/3e/c5/ab/3ec5ab1c4eb0655c5061617e53c87a9e.jpg' 
        },
        { 
          id: 2, 
          name: 'HEXOHM V3 GREEN', 
          description: 'Price 3.0000.000.', 
          url: 'https://i.redd.it/mh9yhddcffbc1.jpeg' 
        },
        { 
          id: 3, 
          name: 'HEXOMH BlUE', 
          description: 'Price 3.200.000', 
          url: 'https://e1.pxfuel.com/desktop-wallpaper/343/638/desktop-wallpaper-breaking-out-the-spring-setup-vaping-hexohm.jpg' 
        },
        { 
          id: 4, 
          name: 'HEXOHM V3 WHITE FREE SLEEVE BAPE', 
          description: 'Price 3.500.000', 
          url: 'https://images.tokopedia.net/img/cache/700/VqbcmM/2021/5/14/ee676abd-05bd-4f0b-8eb5-7d9e53442b42.jpg' 
        },
        { 
          id: 5, 
          name: 'HEXOHM V3 WHITE SPLATTER', 
          description: 'Price 3.500.000', 
          url: 'https://media.karousell.com/media/photos/products/2021/12/11/hexohm_v3_white_splatter_1639218084_1672e84a_progressive.jpg' 
        },
        { 
          id: 6, 
          name: 'HEXOHM X R57 ', 
          description: 'Price 3.500.000', 
          url: 'https://wallpapercave.com/wp/wp5400032.png' 
        }
      ]
    };
  }
};
</script>

<style>
body {
  background-color: rgb(239, 234, 234);
}

.card-container {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 16px; /* Optional: Adjust the space between cards */
}

.card {
  flex-basis: calc(33.33% - 16px); /* Atur lebar kartu dengan ketiga bagian dari wadah dikurangi jarak antar kartu */
}
</style>
