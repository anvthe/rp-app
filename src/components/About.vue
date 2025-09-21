<template>
  <section id="about" class="about-section py-5">
    <div class="container">
      <div class="row align-items-center g-5">
        <!-- Image -->
        <div class="col-md-6 text-center">
          <img
              src="https://source.unsplash.com/600x400/?technology,office"
              class="img-fluid rounded-4 shadow-lg animate-fade"
              alt="About"
          >
        </div>

        <!-- Content -->
        <div class="col-md-6 animate-slide">
          <h2 class="fw-bold mb-3">
            About <span class="text-gradient">Us</span>
          </h2>
          <p class="lead text-muted">
            We are a <strong>leading software company</strong> providing
            innovative solutions to help businesses grow digitally.
          </p>
          <p>
            Our passionate team specializes in crafting cutting-edge
            <strong>web, mobile, and cloud applications</strong> that deliver
            value and empower businesses worldwide.
          </p>
          <a href="#services" class="btn btn-gradient mt-3 px-4 py-2">
            Learn More →
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.about-section {
  background: #f9f9fb;
}

/* Gradient text */
.text-gradient {
  background: linear-gradient(45deg, #00d4ff, #ff007f);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
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

/* Animations */
@keyframes fadeIn {
  from { opacity: 0; transform: scale(0.95); }
  to { opacity: 1; transform: scale(1); }
}
.animate-fade { animation: fadeIn 1.2s ease forwards; }

@keyframes slideIn {
  from { opacity: 0; transform: translateX(60px); }
  to { opacity: 1; transform: translateX(0); }
}
.animate-slide { animation: slideIn 1.2s ease forwards; }
</style>
