<template>
  <div class="about" id="about">
    <Header></Header>
    <Content></Content>
  </div>
</template>

<script>
import Header from "./Header.vue";
import Content from "./Content.vue";

export default{
  name:"about",
  components:{
    Header,
    Content,
  },
};
</script>

