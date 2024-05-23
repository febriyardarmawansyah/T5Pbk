<template>
  <div class="carousel">
    <div v-for="(image, index) in images" :key="index" class="carousel-item">
      <img :src="image.url" :alt="image.alt" class="carousel-image" />
    </div>
  </div>
</template>

<script>
export default {
  name: 'Carousel',
  data() {
    return {
      images: [
        { url: 'https://img1.wsimg.com/isteam/ip/133dd2a3-6070-41c6-ad94-b7158afddea9/00fcc974-03f6-4eaf-8b6f-5cf319926336.jpg/:/rs=w:767,m', alt: 'V3 hex' },
        { url: 'https://vaporesia.com/wp-content/uploads/2019/09/HexOhm-V3-HEXZOO.jpeg', alt: 'Image 2' },
        { url: 'https://img1.wsimg.com/isteam/ip/133dd2a3-6070-41c6-ad94-b7158afddea9/60fdf42b-f078-42b2-8b64-243220608c26.jpg/:/cr=t:13.55%25,l:6.73%25,w:86.54%25,h:76.92%25/rs=w:2480,h:1240,cg:true,m', alt: 'Image 3' },
        { url: 'https://img1.wsimg.com/isteam/ip/133dd2a3-6070-41c6-ad94-b7158afddea9/b3256649-15e9-479f-a356-4c271ee967a6.jpg/:/cr=t:5.36%25,l:0%25,w:100%25,h:89.29%25/rs=w:1200,h:600,cg:true' },
        { url: 'https://img1.wsimg.com/isteam/ip/133dd2a3-6070-41c6-ad94-b7158afddea9/Tipe%20Hexohm.jpg/:/cr=t:0%25,l:0%25,w:100%25,h:100%25/rs=w:1080,cg:true', alt: 'Image 5' }      ]
    }
  }
}
</script>

<style>
.carousel {
  display: flex;
  overflow-x: auto;
  scroll-snap-type: x mandatory;
  padding: 20px 0; /* Ubah padding atas dan bawah */
  margin-bottom: 20px;
}

.carousel-item {
  scroll-snap-align: start;
  flex: none;
  width: 70%; /* Mengurangi lebar item */
  margin-right: 10px;
  border-radius: 12px; /* Meningkatkan ukuran border-radius */
  overflow: hidden;
  display: flex;
  justify-content: center;
  align-items: center;
  box-shadow: 0px 6px 12px rgba(0, 0, 0, 0.15); /* Menyesuaikan bayangan */
}

.carousel-image {
  width: 100%; /* Mengisi ruang secara penuh */
  height: auto; /* Menjaga aspek gambar */
  object-fit: cover;
  border-radius: 12px; /* Meningkatkan ukuran border-radius */
  transition: transform 0.3s ease;
}

.carousel-item:hover .carousel-image {
  transform: scale(1.1); /* Meningkatkan skala pada hover */
}

@media (max-width: 768px) {
  .carousel-item {
    width: calc(80% - 10px); /* Menyesuaikan lebar untuk perangkat seluler */
  }
}

</style>
