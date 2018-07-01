<template>
  <div class="about">
    <h1>page{{msg}} </h1>
    <input type="button" @click="incrment">
  </div>
</template>
<script>
export default {
  data () {
    return {
      i:1
    }

  },
      computed:{
      msg(){
return this.$store.state.count;
      }
    },
    methods:{
      incrment(){
        this.$store.commit("changeCount",this.i++)
      }
    }
}
</script>
