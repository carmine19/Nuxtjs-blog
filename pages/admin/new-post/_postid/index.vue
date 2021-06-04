<template>
  <div>
    <h1>edit-post</h1>
    <!-- componente props centralizzato che richiamo il nostro oggetto newPost tramite la props
     object che abbiamo creato nel componente, qui poi la richiamiamo assegnadogli il nostro oggetto
      che abbiamo in data-->
    <FormPost :post="newPost" />
  </div>
</template>


<script>

export default {
  layout : 'admin',
  data() {
    return {
      newPost : {
        id : '',
        title : 'Edit post',
        description : '',
        cover: '',
      }
    }
  }
}

</script>


<style>

</style>
