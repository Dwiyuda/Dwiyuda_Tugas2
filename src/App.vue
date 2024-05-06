<template>
  <div>
    <h1>Masukkan huruf kapital</h1>
    <div>
      <input type="text" v-model="inputText" placeholder="Masukkan teks">
    </div>
    <div v-if="inputText.length >= 15">
      <h2>Jumlah Karakter: {{ inputText.length }}</h2>
      <p>Teks sudah cukup panjang.</p>
    </div>
    <div v-else>
      <h2>Jumlah Karakter: {{ inputText.length }}</h2>
      <p>Teks belum cukup panjang. Minimal 15 karakter diperlukan.</p>
    </div>
    
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputText: ''
    };
  }
}
</script>

<style>
  body {
    font-family: Arial, sans-serif;
    background-color: lightblue;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
  }

  .container {
    max-width: 600px;
    background-color: #fff;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    padding: 20px;
  }

  h1 {
    text-align: center;
    color: #333;
    margin-bottom: 20px;
  }

  input[type="text"] {
    width: 100%;
    padding: 10px;
    margin-bottom: 20px;
    border: 1px solid #ccc;
    border-radius: 4px;
    box-sizing: border-box;
    font-size: 16px;
  }

  h2 {
    color: #333;
    margin-bottom: 10px;
  }

  p {
    color: #555;
  }

  
</style>
