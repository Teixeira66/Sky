<template>
  <div id="app">
    <table border=1px>
    <tr>
        <td>Name</td>
        <td>UserName</td>
    </tr> 

    </table>
  </div>
</template>

<script>
import Vue from "vue";
import axios from "axios";
import VueAxios from "vue-axios";
Vue.use(VueAxios.axios);
export default {
  name: "list",
  mounted()
  {
      Vue.axios.get('https://jsonplaceholder.typicode.com/users')
      .then((resp)=>{
          console.warn(resp)
      })
  }

}
</script>