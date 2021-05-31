<template>
  <div id="card">
    <div class="container">
      <div class="row">
        <div class="col-lg-4 mb-5" >
          <div class="card" style="width: 18rem;">
            <img :src="cover" class="card-img-top" :alt="title">
            <div class="card-body">
              <h5 class="card-title">{{title}}</h5>
              <p class="card-text">{{description}}</p>
              <!-- per passare i parametri, in questo caso l id, bisogna usare un link di vue come creato
               sotto, cioè     :href="` /posts/${id} `"     -->
              <a :href="` /posts/${id} `" class="btn btn-primary">Go somewhere</a>
            </div>
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

    }
  },

  //le props vanno definite ed usate nei componenti per poi essere riusate quante volte si vuole dinamicamente
  //quindi vanno definite nel componente e poi richiamate dove le si vuole usare, in questo caso nella pagina posts
  props: {
    id : {
      type : String,
      required : true
    },
    title : {
      type : String,
      required : true
    },
    description : {
      type : String,
      required : true
    },
    cover : {
      type : String,
      required : true
    }
  }
}
</script>

<style>

#card {
  margin-top: 100px;

}

</style>
