<template>
  <section class="hero d-flex align-items-center justify-content-center text-center">
    <div class="overlay"></div>
    <div class="content p-4 rounded-4 shadow-lg">
      <h1 class="display-3 fw-bold mb-3 animate-fade">
        We Build <span class="text-gradient">Modern Software</span>
      </h1>
      <p class="lead mb-4 animate-slide">
        Your trusted partner for <strong>Web</strong> & <strong>Mobile Development</strong>
      </p>
      <a href="#services" class="btn btn-gradient btn-lg px-4 py-2 animate-bounce">
        🚀 Get Started
      </a>
    </div>
  </section>
</template>

<style scoped>
/* Hero section background */
.hero {
  position: relative;
  height: 100vh;
  background: url("https://source.unsplash.com/1600x900/?technology,future,innovation") center/cover no-repeat;
  color: #fff;
  overflow: hidden;
}

/* Dark overlay */
.overlay {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(10, 10, 30, 0.7);
  backdrop-filter: blur(3px);
}

/* Hero content box */
.content {
  position: relative;
  z-index: 2;
  max-width: 800px;
  background: rgba(255, 255, 255, 0.05);
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.15);
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
  box-shadow: 0 8px 25px rgba(0, 212, 255, 0.5);
}

/* Animations */
@keyframes fadeIn {
  from { opacity: 0; transform: translateY(30px); }
  to { opacity: 1; transform: translateY(0); }
}
.animate-fade { animation: fadeIn 1.2s ease forwards; }

@keyframes slideUp {
  from { opacity: 0; transform: translateY(50px); }
  to { opacity: 1; transform: translateY(0); }
}
.animate-slide { animation: slideUp 1.5s ease forwards; }

@keyframes bounceIn {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-8px); }
}
.animate-bounce { animation: bounceIn 2s infinite; }
</style>
