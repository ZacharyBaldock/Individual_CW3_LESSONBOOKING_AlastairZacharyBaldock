<template>
<main>
    <div v-for="product in products" :key="product.id">
        <h2>{{product.title}}</h2>
        <figure>
            <img v-bind:src="product.image" />
        </figure>
        <p v-html="product.description"></p>
        <p>Price: {{ product.price }}</p>
        <p>Available stock: {{ product.availableInventory }}</p>
        <button @click="add(product)">Add to cart</button>
    </div>
</main>
</template>

<script>
export default {
    name: "ProductList",
    data() {
        return {
          products: [
   {
    "id": 1001,
    "title": "Maths",
    "description": "Located in Hursthampton, For those who have trouble with maths",
    "price": 25,
    "image": "https://thumbs.dreamstime.com/b/math-mathematics-word-vintage-letterpress-wood-type-against-number-background-37860245.jpg",
    "availableInventory": 5,
    "rating": 5 
  },
  {
    "id": 1002,
    "title": "Chemistry",
    "description": "Located in Hedgeven, For those who have trouble with Chemistry",
    "price": 25,
    "image": "https://static.vecteezy.com/system/resources/previews/000/098/099/original/free-chemistry-vector.jpg",
    "availableInventory": 5,
    "rating": 4 
  },
  {
    "id": 1003,
    "title": "Phsisics",
    "description": "Located in Highchedown, For those who have trouble with physics",
    "price": 25,
    "image": "https://www.nicepng.com/png/detail/268-2688182_school-project-physics-royalty-free-vector-clip-art.png",
    "availableInventory": 5,
    "rating": 3
  },
  {
    "id": 1004,
    "title": "Biology",
    "description": "Located in Horsson, For those who need to catch up in Biology",
    "price": 25,
    "image": "https://moodle.gtni.edu.eg/pluginfile.php/2720/course/overviewfiles/biology-800x393.jpg",
    "availableInventory": 5,
    "rating": 4
  },
  {
    "id": 1005,
    "title": "English",
    "description": "Located in Haygton, For those who need to catch up in English class",
    "price": 25,
    "image": "https://st2.depositphotos.com/3591429/5244/i/600/depositphotos_52449961-stock-photo-peoples-arms-holding-word-english.jpg",
    "availableInventory": 5,
    "rating": 5
  },
  {
    "id": 1006,
    "title": "French",
    "description": "Located in Hawesfern, So the subject isn't french to you",
    "price": 25,
    "image": "https://lh3.googleusercontent.com/proxy/9MQGTcKtKv3a6qqeaRdI1UFbfJs0CllWn5XSJALpW9-pMLyMd9Uf7ztapprrzSG877IT8kCgKZ0NNMFS6gSEH7Wa2TC4Y_WSrE6r7wk",
    "availableInventory": 5,
    "rating": 4
  },
  {
    "id": 1007,
    "title": "Arabic",
    "description": "Located in Hesswan, its quite a beautiful languge",
    "price": 25,
    "image": "https://media-whichmedia.s3.ap-southeast-1.amazonaws.com/media/large/e/0/e0814526963e.jpeg",
    "availableInventory": 5,
    "rating": 3
  },
  {
    "id": 1008,
    "title": "Music",
    "description": "Located in Hesswan, if your skills need tuning up",
    "price": 25,
    "image": "https://i.pinimg.com/originals/90/81/e0/9081e0782766430555cffcb3129996a8.jpg",
    "availableInventory": 5,
    "rating": 4
  },
  {
    "id": 1009,
    "title": "History",
    "description": "Located in Haygton, So the subject is not quite such a mystery",
    "price": 25,
    "image": "https://lh3.googleusercontent.com/proxy/jBJ9G14qT2MMGLRsHg6XTvmtZsjoGFQLsMMxk6VgGXxBi5BdL9j7w88BOywT9MjU3iQL1ubcqwyrxC8aS1tbpS1b",
    "availableInventory": 5,
    "rating": 5
  },
  {
    "id": 1010,
    "title": "IT",
    "description": "Located in Hursthampton, Quite the employable Skill",
    "price": 25,
    "image": "https://lh3.googleusercontent.com/proxy/3LgIoUOwUOnW1zRoZIzXVjKb5nNOwd06g0LhYOyJVtfFc93M5hp4kNrgiAY6fE6OyzaEEOHejdc4hXihz6Nayks2Qr-_9ZU",
    "availableInventory": 5,
    "rating": 5
  },

      ],

    };

  },
  methods: {
    add(product) {
      console.log("added product", product.id);
      this.$emit('addProduct',product);
    },
  },
};
</script>


