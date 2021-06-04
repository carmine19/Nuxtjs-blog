<template>
  <div>
    <form>
      <div class="mb-3">
        <label for="id" class="form-label">{{newPost.id}}</label>
        <input v-model="newPost.id" class="form-control" type="text" placeholder="id">
      </div>
      <div class="mb-3">
        <label for="title" class="form-label">{{newPost.title}}</label>
        <input v-model="newPost.title" class="form-control" type="text" placeholder="title">
      </div>

      <div class="mb-3">
        <label for="description" class="form-label">{{newPost.description}}</label>
        <input v-model="newPost.description" class="form-control" type="text" placeholder="description">
      </div>

      <div class="mb-3">
        <label for="cover" class="form-label">{{newPost.cover}}</label>
        <input v-model="newPost.cover" class="form-control" type="text" placeholder="cover">
      </div>


      <button @click="save" type="" class="btn btn-primary">Submit</button>

      <button @click="cancel" type="reset" class="btn btn-primary">Cancel</button>
    </form>
  </div>
</template>

<script>
export default {
  name: "FormPost",

  data() {
    return {
      newPost : {
        id : '',
        title : '',
        description : '',
        cover: '',
      }
    }
  },

  methods : {
    save() {
      console.log(this.newPost)
    },
    cancel() {
      this.$router.push('/admin')
    }
  }
}
</script>

<style scoped>

</style>
