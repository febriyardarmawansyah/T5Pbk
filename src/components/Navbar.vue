<template>
  <nav class="navbar">
    <div class="logo">
      <span class="logo-highlight">FEBRIYAR</span> HEXZOO
    </div>
    <ul class="nav-links">
      <li><a href="#home">HOME</a></li>
      <li><a href="#products">PRODUCT</a></li>
      <li><a href="#contact">CONTACT</a></li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'Navbar'
}
</script>

<style>
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #010101;
  padding: 40px 100px; /* Menambahkan padding lebih besar */
}

.logo {
  color: #efe8e8;
  font-size: 24px;
  font-family: 'Broadway';
}

.logo-highlight {
  color: #c8ff00; /* Warna berbeda untuk teks "FEBRIYAR" */
}

.nav-links {
  list-style: none;
  display: flex;
  margin: 0; /* Menghapus margin default */
  padding: 0; /* Menghapus padding default */
}

.nav-links li {
  margin: 0 15px; /* Menambahkan jarak antar item navbar */
}

.nav-links a {
  color: #f5f50a;
  text-decoration: none;
  font-size: 24px; /* Memperbesar ukuran font untuk link */
}

.nav-links a:hover {
  text-decoration: underline; /* Menambahkan garis bawah saat hover */
}
</style>
