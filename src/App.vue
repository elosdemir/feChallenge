<template>
  <b-container id="app">
    <Header />
    <Banner />
    <BreadCrumb />
    <b-container>
      <b-row>
        <b-col  lg="8" sm="12" md="12" >
          <Form />
        </b-col>
        <b-col  lg="4" sm="12" md="12" >
          <Collapse />
        </b-col>
      </b-row>
    </b-container>
  </b-container>
</template>

<script>
import Header from './components/Header';
import Banner from './components/Banner';
import Form from './components/Form';
import Collapse from './components/Collapse';
import BreadCrumb from './components/BreadCrumb';

export default {
  name: 'App',
  components: {
    Header,
    Banner,
    Form,
    Collapse,
    BreadCrumb
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: 0 auto;

}
</style>
