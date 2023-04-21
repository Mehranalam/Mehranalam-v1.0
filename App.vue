<template>
  <div class="holder">
    <div class="diva">
      <div class="rowC">
        <i class="icon-mehranalam"></i>
        <h2>Mehranalambeigi-V1.0</h2>
      </div>
      <ul>
        <li> <router-link  to="/"> home</router-link></li>
        <li> <router-link  to="/demo"> resume</router-link></li>
        <li> <router-link  to="/demo">Projects</router-link></li>
        <li> <router-link  to="/demo">project request</router-link></li>
        <li> <router-link  to="/demo">code part</router-link></li>
      </ul>
    </div>

    <router-view></router-view>

    <theFooter />

  </div>
</template>

<script>
import theFooter from './components/Footer.vue'


export default {
  name: 'App',
  components: {
    theFooter
  }
}
</script>

<style scoped>
.diva {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  margin-top: 3%;
}
.rowC {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
.rowC:hover {
  cursor: pointer;
}
ul li{
  font-family:'IRANYekanMedium' ,Arial, Helvetica, sans-serif;
  display: inline;
  margin: 9px;
}
ul li:hover {
  color: #A0BCC2;
  cursor: pointer;
}

.blog {
  display:inline-block;
  margin: 10%;
  /* margin-right: 5%; */
}
.box-holder {
  display: flex;
}
.box-holder img {
  border-radius: 16px;
}
.content {
  display: flex;
  flex-direction: column;
  margin-right: 4%;
}
.card {
  display: flex;
  flex-direction: row;
  margin-bottom: 5%;
  justify-content: center;
}
.child {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  flex-direction: column;
  margin-bottom: 5%;
  width: 200px;
  margin: 3%;
}
.card img {
  border-radius: 16px;
}
</style>
