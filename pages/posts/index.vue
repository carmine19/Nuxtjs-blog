<template>
  <div>
    <h1 class="text-center">pagina post</h1>


    <div id="card">
      <div class="container">
        <div class="row">
          <!-- questo è il componente card, i suoi parametri che passa sono definiti con le props
           ricorda bene che le props quando passi un array di oggetti va passato il v-bind, cioè
            :id="post.id" o v-bind:id="post.id", sono la stessa cosa ma servono ad indicare che il paremetro
            è di tipo dinamico o vue-->
          <Card v-for="(post, index) in posts"  :id="post.id" :title="post.title" :description="post.description" :cover="post.cover" />
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
          {id : '2', title : 'titolo post', description : 'lorem ipsum dolor sit amet', cover: 'https://source.unsplash.com/random/200x200'},
          {id : '3', title : 'titolo post', description : 'lorem ipsum dolor sit amet', cover: 'https://source.unsplash.com/random/200x200'},
          {id : '4', title : 'titolo post', description : 'lorem ipsum dolor sit amet', cover: 'https://source.unsplash.com/random/200x200'},
          {id : '5', title : 'titolo post', description : 'lorem ipsum dolor sit amet', cover: 'https://source.unsplash.com/random/200x200'},
          {id : '6', title : 'titolo post', description : 'lorem ipsum dolor sit amet', cover: 'https://source.unsplash.com/random/200x200'},
        ]
      }
    }
}
</script>




<style >
#card {
  margin-top: 100px;

}
</style>
