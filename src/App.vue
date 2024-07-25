<template>
  <div id="app">
    <nav>
      <ul>
        <li><router-link to="/">Anasayfa</router-link></li>
        <li><router-link to="/invoices">Faturalar</router-link></li>
      </ul>
    </nav>

    <router-view />
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style lang="scss">
@import '@/assets/scss/main.scss';

#app {
  max-width: 960px;
  margin: 0 auto;
  padding: 20px;
}

nav {
  ul {
    list-style-type: none;
    padding: 0;
    
    li {
      display: inline-block;
      margin-right: 10px;
      
      a {
        text-decoration: none;
        color: $primary-color;
        
        &:hover {
          text-decoration: underline;
        }
      }
    }
  }
}
</style>