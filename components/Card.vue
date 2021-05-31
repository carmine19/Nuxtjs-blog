<template>
  <div id="card">
    <div class="container">
      <div class="row">
        <div class="col-lg-4 mb-5" v-for="i in 6">
          <div class="card" style="width: 18rem;">
            <img src="https://picsum.photos/200/200" class="card-img-top" alt="...">
            <div class="card-body">
              <h5 class="card-title">Card title</h5>
              <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
              <a href="#" class="btn btn-primary">Go somewhere</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style>

#card {
  margin-top: 100px;

}

</style>
