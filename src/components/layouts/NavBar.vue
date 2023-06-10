<template>
  <div class="navbar-container">
    <nav>
      <div class="nav-links">
        <router-link to="/" class="nav-link">Home</router-link>
        <router-link to="/new-anime" class="nav-link">New Anime</router-link>
      </div>
      <div class="logo-container">
        <img class="logo1" src="./Screen Shot 2023-06-10 at 4.35.16 AM.png" alt="Logo">
      </div>
    </nav>
  </div>
</template>

<style>
.navbar-container {
  background-color: #05708C;
  color: #fff;
  padding: 10px;
}

nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.nav-links {
  display: flex;
  align-items: center;
}

.nav-link {
  color: #fff;
  text-decoration: none;
  transition: color 0.3s ease;
  margin-right: 10px; /* Adjust the margin as needed */
}

.nav-link:hover {
  color: #aaa;
}

.logo-container {
  display: flex;
  align-items: right;
}

.logo1 {
  height: 60px;
  margin-left: auto; /* Move the logo to the right */
}
</style>
