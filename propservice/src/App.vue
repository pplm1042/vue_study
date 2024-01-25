<template>

  <div class="menu">
    <a v-for="(menu, index) in menus" :key=index>{{ menu }}</a>
  </div>
  <div v-for="(product, index) in products" :key=index>
    <h4 :style=titleStyle>{{ product.name }}</h4>
    <p>{{ product.price }} 만원</p>
    <button @click=product.report++ @mouseover="style=titleStyle">허위매물신고</button> <span>신고수 : {{ product.report }}</span>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      menus : ['Home', 'About', 'Contact'],
      products : [ 
        {
        'name' : '역삼동원룸',
        'price' : '50',
        'report' : 0,
      },
      {
        'name' : '천호동원룸',
        'price' : '가격은 아무거나',
        'report' : 0,
      },
      {
        'name' : '마포구원룸',
        'price' : '가격은 아무거나',
        'report' : 0,
      }, {
        'name' : '역삼동원룸',
        'price' : '50'
      },
      {
        'name' : '천호동원룸',
        'price' : '가격은 아무거나'
      },
      {
        'name' : '마포구원룸',
        'price' : '가격은 아무거나'
      }, {
        'name' : '역삼동원룸',
        'price' : '50'
      },
      {
        'name' : '천호동원룸',
        'price' : '가격은 아무거나'
      },
      {
        'name' : '마포구원룸',
        'price' : '가격은 아무거나'
      },
      {
        'name' : '역삼동원룸',
        'price' : '50'
      },
      {
        'name' : '천호동원룸',
        'price' : '가격은 아무거나'
      },
      {
        'name' : '마포구원룸',
        'price' : '가격은 아무거나'
      }],
      titleStyle : {
        'color' : 'blue',
        'font-size' : '20px'
      }
            
    }
  },
  components: {
    
  }
}
</script>



<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.menu {
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}
.menu a {
  color: white;
  padding: 10px;
}
</style>
