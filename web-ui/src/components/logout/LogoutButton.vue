<template>
<table class="sw-logout-button">
  <tr>
    <td class="sw-user sw-role p4" >{{$store.state.role}}</td>
    <td class="sw-power" rowspan="2"> <clr-icon shape="power" size="24" @click="logout" style="color:white"/></td>
  </tr>
  <tr>
    <td class="sw-user sw-name p3" >{{$store.state.userName}}</td>
  </tr>
</table>
</template>

<script>
  import router from '@/router'

  export default {
    methods:{
      logout(){
        router.push("/login")
      }
    }
  }
</script>

<style scoped lang="scss">
@import "~@/assets/styles/_vars.scss";
.sw-logout-button{
  margin:16px;
  .sw-user{
    color:#fff;
    text-align: right;
    padding:0 5px;
  }
  .sw-role{
    color:#999;
    font-weight:bold;
    text-transform: uppercase;
  }
  .sw-power{
    cursor:pointer;
    padding:3px;
    background-color:#ee6146;
    border:0px solid #ccc;
    border-radius:2px;
  }
}
</style>