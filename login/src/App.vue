<template>
  <router-view />
</template>

<script lang="ts" setup>
</script>
<script lang="ts">
export default{
  created(){
      if(false){
        console.log("AUTH reroute HOME test")
        this.$router.push("/");
      }
      else{
        this.$router.push("/login");
        console.log("NO AUTH REROUTE LOGIN")
      }
  }
}

</script>

<style>
html, body {
  width: 100%;
  height: 100%;
  background-color: rgb(48, 48, 48);
}
</style>
