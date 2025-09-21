<template>
  <section id="services" class="py-5 bg-light">
    <div class="container text-center">
      <h2 class="mb-4">Our Services</h2>
      <div class="row">
        <div class="col-md-4 mb-3" v-for="service in services" :key="service.title">
          <div class="card h-100 shadow-sm border-0">
            <div class="card-body">
              <div class="mb-3 fs-1">{{ service.icon }}</div>
              <h5 class="card-title">{{ service.title }}</h5>
              <p class="card-text">{{ service.desc }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const services = [
  { icon: "💻", title: "Web Development", desc: "High-performing and responsive websites." },
  { icon: "📱", title: "Mobile Apps", desc: "Cross-platform apps for Android & iOS." },
  { icon: "☁️", title: "Cloud Solutions", desc: "Scalable and secure cloud systems." },
]
</script>
