<template>
  <div>
      <div class="card">
        <img :src="cover" class="card-img-top" :alt="title">
        <div class="card-body">
          <h5 class="card-title">{{title}}</h5>
          <p class="card-text">{{description}}</p>
          <!-- per passare i parametri, in questo caso l'id, utilizziamo il nuxt-link andando a specificare
               che il tag e di tipo 'a' e poi passiamo l'id come parametro legato a post, ricordati che
               precedentemente hai già definito nella cartella post sia la rotta priincipale che l'id-->
          <NuxtLink tag="a" :to=" /posts/ + this.id" class="btn btn-primary">Post numero: {{id}}</NuxtLink>
          <button v-if="" @click="linkToEdit(id)" class="btn btn-danger">edit</button>
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

  methods : {
    linkToEdit(id) {
      this.$router.push('/admin/new-post/' + id)
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
    },
    isAdmin : {
      type : Boolean,
      default : false
    }
  }
}
</script>

<style>



</style>
