<template>
  <div id="app">
    <header class="header"> <div class="header-content"> <div class="header-left">Header</div> <nav class="header-right"> <router-link to="/page1" active-class="active">Page 1</router-link> <router-link to="/page2" active-class="active">Page 2</router-link> <router-link to="/page3" active-class="active">Page 3</router-link> </nav> </div> </header>
    <aside class="menu">
      <a href="#">Section 1</a>
      <a href="#">Section 2</a>
      <a href="#">Section 3</a>
      <a href="#">Section 4</a>
    </aside>
    <main class="content">
      
      <router-view></router-view>
    </main>
    <footer class="footer">
      Footer
    </footer>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
body {
  font-family: Arial, sans-serif;
  margin: 40px;
  padding: 0;
}
.header { background-color: #f1f1f1; padding: 10px; text-align: center; border: 1px solid #ccc; /* Add border */ } .header-content { display: flex; justify-content: space-between; align-items: center; } .header-left { font-weight: bold; } .header-right a { margin: 0 10px; text-decoration: none; color: black; } .header-right a.active { color: red; }
.menu {
  float: left;
  width: 20%;
  background-color: #f9f9f9;
  padding: 10px;
  border: 1px solid #ccc;
  height: 300px;
}
.menu a {
  display: block;
  padding: 8px;
  text-decoration: none;
  color: black;
  border: 1px solid #ccc;
}
.menu a:hover {
  background-color: #81d9df;
}
.content {
  margin-left: 20%;
  padding: 10px;
  border: 1px solid #ccc;
  height: 300px;
  justify-content: center;
  text-align: center;
  align-content: center;
  color: purple
}
.nav a {
  margin: 0 10px;
  text-decoration: none;
  color: black;
}
.nav a.active {
  color: red;
}
.footer {
  background-color: #f1f1f1;
  padding: 10px;
  text-align: center;
  border: 1px solid #ccc;
}
</style>
