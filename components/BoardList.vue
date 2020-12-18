<template>
  <p>{{msg}}</p>
</template>

<script>
import axios from 'axios'

export default {
    data (){
        return {
          msg: 'hi'
        }
    },
    created(){
      this.init()
    },
    methods : {
      init(){
        axios.post('api/hello.json').then(res => {
          this.msg = res.data
          console.log(res)
        })
      }
    },
}
</script>

<style>

</style>