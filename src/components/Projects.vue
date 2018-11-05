<template>
    <div class="list-group">
      <div v-for="(posts, index) in info" :key="index">
        <div v-for="(post, index) in posts.project_lists" :key="index">
          <div class="card">
            <div class="card-body">
              <h4 class="card-title">{{post.title}}</h4>
              <h6 class="card-subtitle mb-2 text-muted">{{ post.region.bundesland }}</h6>
              <p class="card-text">{{ post.description.slice(0,500) }}</p>
              <a href="#" class="card-link">{{post.bereich.group}}</a>
              <a href="#" class="card-link">{{post.bereich.group_type}}</a>
            </div>
          </div>
        </div>
        
      </div>
        
    </div>
    
</template>

<script>
import axios from "axios/dist/axios.min.js";
    export default {
  name: "Projects",
  props: {
    msg: String
  },
  data () {
    return {
      title: 'Projects ',
      info: [],
      products:[
      {
        productTitle:"ABCN",
        image       : require('../assets/images/product1.jpeg'),
        productId:1
      },
      {
        productTitle:"KARMA",
        image       : require('../assets/images/product2.jpeg'),
        productId:2
      },
      {
        productTitle:"Tino",
        image       : require('../assets/images/product3.jpeg'),
        productId:3
      },
      {
        productTitle:"EFG",
        image       : require('../assets/images/product4.jpeg'),
        productId:4
      },
      {
        productTitle:"MLI",
        image       : require('../assets/images/product5.jpeg'),
        productId:5
      },
      {
        productTitle:"Banans",
        image       : require('../assets/images/product6.jpeg'),
        productId:6
      }
      ]
    }

  },
  mounted() {
    axios
      .get('http://127.0.0.1:5000/home')
      .then(response => (this.info = response))
  }
};
</script>
