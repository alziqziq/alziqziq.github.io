<template>
  <div class="hello">
    <h1><b>Vue-Paginate-Al</b></h1>
    <h5>by: Muhammad Al Ziqri</h5>
    <br>

    <a href="https://github.com/alziqziq/vue-paginate-al">
      <img src="@/assets/github.png" alt="" width="70px" height="70px">
      <br>
    </a>
    <h5><b>Check Your Console Log</b></h5>
    <hr>

    <h3>Default</h3>
    <h6>{{ contoh1 }}</h6>
    <vue-paginate-al :totalPage="10" @btnClick="goToFunction"></vue-paginate-al>
    <hr>

    <h3>With background color and without button next/prev</h3>
    <h6>{{ contoh2 }}</h6>
    <vue-paginate-al :totalPage="15" activeBGColor="success" :withNextPrev="false"></vue-paginate-al>
    <hr>

    <h3>With current page</h3>
    <h6>{{ contoh5 }}</h6>
    <vue-paginate-al :totalPage="10" :currentPage="5" @btnClick="goToFunction"></vue-paginate-al>
    <hr>

    <h3>With single data</h3>
    <h6>{{ contoh3 }}</h6>
    <vue-paginate-al :totalPage="20" :myData="'myname'" @btnClick="goToFuncWithData"></vue-paginate-al>
    <hr>

    <h3>With multiple data</h3>
    <h6>{{ contoh4 }}</h6>
    <vue-paginate-al :totalPage="20" :myData="['myname', 'myemail']" @btnClick="goToFuncWithMultipleData"></vue-paginate-al>
  </div>
</template>

<script>
export default {
  name: 'VuePaginteAl',
  data() {
    return {
      contoh1: '<vue-paginate-al :totalPage="10" @btnClick="goToFunction"></vue-paginate-al>',
      contoh2: '<vue-paginate-al :totalPage="15" activeBGColor="success" :withNextPrev="false"></vue-paginate-al>',
      contoh3: '<vue-paginate-al :totalPage="20" :myData="\'myname\'" @btnClick="goToFuncWithData"></vue-paginate-al>',
      contoh4: '<vue-paginate-al :totalPage="20" :myData="[\'myname\', \'myemail\']" @btnClick="goToFuncWithMultipleData"></vue-paginate-al>',
      contoh5: '<vue-paginate-al :totalPage="10" :currentPage="5" @btnClick="goToFunction"></vue-paginate-al>'
    }
  },
  methods : {
    goToFunction : function(n) {
      console.log(n);
    },

    goToFuncWithData : function(n, data) {
      console.log(n, data);
    },

    goToFuncWithMultipleData : function(n, data){
      console.log(n, data[0], data[1]);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
