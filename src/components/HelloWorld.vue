<template>
  <div class="hello" @click="clicks" >
    <h1>{{ msg }}</h1>
    <p>
      For a guide and recipes on how to configure / customize this project,<br>
      check out the    
    </p>
    <div>
      {{aa}}
    </div>
  </div>

</template>

<script>
const axios = require('axios');
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      aa: 'Hello Vue!'
    }
  },
  methods:{
    clicks: function(e){
        console.log(1232322)
      axios.get('http://localhost:3000/news')
      .then(res=>{
        console.log(res)
        this.aa = res.data
      })
      
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

