<template>
  <div>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark text-center">
      <NuxtLink to="/"  class="navbar-brand">Logo</NuxtLink>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item active">
           <NuxtLink to="/" class="nav-link">Home</NuxtLink>
          </li>
          <li class="nav-item">
            <NuxtLink to="/posts" class="nav-link">Blog</NuxtLink>
          </li>

        </ul>
      </div>
    </nav>
  </div>
</template>


<script>

</script>

<style>


</style>
