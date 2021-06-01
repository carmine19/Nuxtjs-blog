<template>
  <div>
    <section id="hero-post">
      <div class="container">
        <div class="row">
          <div class="col">
            <h1>Blog</h1>
          </div>
        </div>
      </div>
    </section>


    <div id="card" v-if="this.load">
      <div class="container text-center">
        <div class="row d-flex justify-content-center">
          <div v-for="(post, index) in posts" class="mb-5" :class="posts ? 'col-lg-4' : 'col-lg-6' " >
            <!-- questo è il componente card, i suoi parametri che passa sono definiti con le props
           ricorda bene che le props quando passi un array di oggetti va passato il v-bind, cioè
            :id="post.id" o v-bind:id="post.id", sono la stessa cosa ma servono ad indicare che il paremetro
            è di tipo dinamico o vue-->
            <Card  :id="post.id" :title="post.title" :description="post.description" :cover="post.cover"  />

          </div>
        </div>
      </div>
    </div>

  </div>
</template>


<script>
export default {
    data() {
      return {
        posts : [
          {id : '1', title : 'titolo post', description : 'lorem ipsum dolor sit amet', cover: 'https://source.unsplash.com/random/200x200'},
          {id : '2', title : 'titolo post', description : 'lorem ipsum dolor sit amet', cover: 'https://source.unsplash.com/user/erondu/200x200'},
          {id : '3', title : 'titolo post', description : 'lorem ipsum dolor sit amet', cover: 'https://source.unsplash.com/200x200/?nature,wild'},
          {id : '4', title : 'titolo post', description : 'lorem ipsum dolor sit amet', cover: 'https://source.unsplash.com/collection/190727/200x200'},
          {id : '5', title : 'titolo post', description : 'lorem ipsum dolor sit amet', cover: 'https://source.unsplash.com/daily/200x200'},
          {id : '6', title : 'titolo post', description : 'lorem ipsum dolor sit amet', cover: 'https://source.unsplash.com/200x200/?nature,water'},
        ],
        load : false,
      }
    },

  mounted() {
      this.load = true
  }
}
</script>




<style >
#card {
  margin-top: 100px;

}

#hero-post {
  background-image: url("assets/bg/bg.jpg");
  background-position: center center;
  background-repeat: no-repeat;
  background-size: cover;
  min-height: 500px;
}

#hero-post .container .row .col {
  display: flex;
  justify-content: center;
}

#hero-post .container .row .col h1 {
  color: white;
}
</style>
