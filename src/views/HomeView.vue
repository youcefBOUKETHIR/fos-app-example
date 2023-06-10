<template>
  <div class="container">
    <div class="header">
      <h1 class="title">My Anime List</h1>
      
    </div>
    <anime-cards></anime-cards>
  </div>
</template>

<style>
.container {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
}

.header {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.title {
  color: #333;
  font-size: 24px;
  margin-bottom: 20px;
}



.anime-card {
  background-color: #f2f2f2;
  padding: 10px;
  border-radius: 5px;
  transition: background-color 0.3s, transform 0.3s;
  cursor: pointer;
}

.anime-card:hover {
  background-color: #e0e0e0;
  transform: translateY(-5px);
}


</style>
