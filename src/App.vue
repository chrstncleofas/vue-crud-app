<template>
  <div id="app">
    <Header />
    <router-view/>
  </div>
</template>

<script>
import Header from './components/layout/Header';
export default {
  name:"app",
  components: {
    Header
  }
}
</script>


<style>
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  body {
    font-family: Arial, Helvetica, sans-serif;
    line-height: 1.4;
  }

  .btn {
    display: inline-block;
    border: none;
    background: #555;
    color: #fff;
    padding: 7px 20px;
    cursor: pointer;
  }

  .btn:hover {
    background: #666;
  }

  .container{
    max-width: 1100px;
    margin: 0 auto;
    overflow: hidden;
  }
  .container .h-title{
    margin-top: 20px;
    margin-bottom: 20px;
    text-align: center;
  }
  .container .p-content{
    margin-top: 20px;
    padding: 17px;
    margin-bottom: 20px;
    text-align: center;
    letter-spacing: 2px;
    line-height: 1.4;
  }

</style>
