<template>
  <section id="portfolio" class="py-5">
    <div class="container text-center">
      <h2 class="mb-4">Our Projects</h2>
      <div class="row g-3">
        <div class="col-md-4" v-for="n in 6" :key="n">
          <img :src="`https://source.unsplash.com/400x300/?technology,${n}`" class="img-fluid rounded shadow" alt="Project">
        </div>
      </div>
    </div>
  </section>
</template>
