<template>
  <section id="portfolio" class="portfolio-section py-5">
    <div class="container text-center">
      <!-- Section Title -->
      <h2 class="fw-bold mb-5">
        Our <span class="text-gradient">Projects</span>
      </h2>

      <!-- Portfolio Grid -->
      <div class="row g-4">
        <div
            class="col-sm-6 col-md-4"
            v-for="(project, index) in projects"
            :key="index"
        >
          <div class="portfolio-card shadow-lg">
            <img
                :src="project.image"
                class="img-fluid rounded-4"
                :alt="project.title"
            >
            <!-- Overlay -->
            <div class="overlay d-flex flex-column justify-content-center align-items-center text-center p-3">
              <h5 class="fw-bold mb-2">{{ project.title }}</h5>
              <p class="small text-light">{{ project.category }}</p>
              <a :href="project.link" target="_blank" class="btn btn-gradient btn-sm mt-2">
                View More →
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const projects = [
  {
    title: "AI Dashboard",
    category: "Web App",
    image: "https://source.unsplash.com/400x300/?ai,technology",
    link: "#"
  },
  {
    title: "E-Commerce Platform",
    category: "Web Design",
    image: "https://source.unsplash.com/400x300/?ecommerce,website",
    link: "#"
  },
  {
    title: "Healthcare Mobile App",
    category: "Mobile",
    image: "https://source.unsplash.com/400x300/?healthcare,app",
    link: "#"
  },
  {
    title: "Cloud Automation",
    category: "Cloud",
    image: "https://source.unsplash.com/400x300/?cloud,server",
    link: "#"
  },
  {
    title: "Crypto Exchange",
    category: "FinTech",
    image: "https://source.unsplash.com/400x300/?crypto,finance",
    link: "#"
  },
  {
    title: "Smart IoT System",
    category: "IoT",
    image: "https://source.unsplash.com/400x300/?iot,smart",
    link: "#"
  }
]
</script>

<style scoped>
.portfolio-section {
  background: #f9f9fb;
}

/* Gradient text */
.text-gradient {
  background: linear-gradient(45deg, #00d4ff, #ff007f);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

/* Portfolio Card */
.portfolio-card {
  position: relative;
  overflow: hidden;
  border-radius: 1rem;
  transition: transform 0.4s ease, box-shadow 0.4s ease;
}
.portfolio-card img {
  transition: transform 0.4s ease;
}
.portfolio-card:hover img {
  transform: scale(1.1);
}
.portfolio-card:hover {
  transform: translateY(-6px);
  box-shadow: 0 15px 35px rgba(0, 0, 0, 0.2);
}

/* Overlay */
.overlay {
  position: absolute;
  inset: 0;
  background: rgba(15, 15, 30, 0.8);
  opacity: 0;
  transition: opacity 0.4s ease;
  border-radius: 1rem;
  color: #fff;
}
.portfolio-card:hover .overlay {
  opacity: 1;
}

/* Gradient button */
.btn-gradient {
  background: linear-gradient(45deg, #00d4ff, #ff007f);
  border: none;
  color: #fff;
  font-weight: 600;
  border-radius: 50px;
  transition: all 0.3s ease;
}
.btn-gradient:hover {
  transform: scale(1.05);
  box-shadow: 0 6px 20px rgba(0, 212, 255, 0.4);
}
</style>
