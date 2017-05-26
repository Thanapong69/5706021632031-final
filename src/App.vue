<template>
  <div id="app">
    <banner></banner>
    <add-menu :add="AddList"></add-menu>
    <menus :menu="menu" :remove="RemoveList"></menus>
  </div>

</template>

<script>
import Banner from './components/Banner'
import Menus from './components/Menus'
import AddMenu from './components/AddMenu'

export default {
  data () {
    return {
      menu: []
    }
  },
  components: {
    Banner,
    Menus,
    AddMenu
  },
  methods: {
    AddList: function (name, phone, email) {
      var newData = {
        name: name,
        phone: phone,
        email: email
      }
      this.menu.push(newData)
    },
    RemoveList: function (index) {
      this.menu.splice(index, 1)
    }
  }
}
</script>

<style>
html {
  height: 100%;
}

body {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
}

#app {
  color: #FF6600;
  margin-top: -300px;
  max-width: 1000px;
  font-family: Source Sans Pro, Helvetica, sans-serif;
  text-align: left;
}

#app a {
  color: #42b983;
  text-decoration: none;
}

.logo {
  width: 100px;
  height: 100px
}
</style>
