<template>
  <section id="services" class="services-section py-5">
    <div class="container text-center">
      <!-- Heading -->
      <h2 class="fw-bold mb-5">
        Our <span class="text-gradient">Services</span>
      </h2>

      <!-- Services Grid -->
      <div class="row g-4">
        <div
            class="col-md-4"
            v-for="service in services"
            :key="service.title"
        >
          <div class="service-card p-4 h-100">
            <div class="icon-circle mx-auto mb-3">
              <span class="fs-1">{{ service.icon }}</span>
            </div>
            <h5 class="fw-bold mb-2">{{ service.title }}</h5>
            <p class="text-muted">{{ service.desc }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const services = [
  { icon: "💻", title: "Web Development", desc: "High-performing, modern and responsive websites." },
  { icon: "📱", title: "Mobile Apps", desc: "Cross-platform mobile apps for Android & iOS." },
  { icon: "☁️", title: "Cloud Solutions", desc: "Scalable, secure and innovative cloud systems." },
]
</script>

<style scoped>
.services-section {
  background: #f9f9fb;
}

/* Gradient text */
.text-gradient {
  background: linear-gradient(45deg, #00d4ff, #ff007f);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

/* Service Card */
.service-card {
  background: rgba(255, 255, 255, 0.9);
  border-radius: 1rem;
  transition: all 0.3s ease;
  box-shadow: 0 6px 20px rgba(0, 0, 0, 0.05);
}
.service-card:hover {
  transform: translateY(-8px) scale(1.03);
  box-shadow: 0 15px 35px rgba(0, 0, 0, 0.15);
}

/* Icon Circle */
.icon-circle {
  width: 80px;
  height: 80px;
  background: linear-gradient(135deg, #00d4ff, #ff007f);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #fff;
  box-shadow: 0 8px 20px rgba(0, 212, 255, 0.4);
  transition: transform 0.3s ease;
}
.service-card:hover .icon-circle {
  transform: rotate(10deg) scale(1.1);
}
</style>
