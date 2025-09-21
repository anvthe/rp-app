<template>
  <nav class="navbar navbar-expand-lg navbar-dark fixed-top custom-navbar shadow">
    <div class="container">
      <!-- Brand -->
      <a class="navbar-brand fw-bold fs-3 d-flex align-items-center" href="#">
        🚀 <span class="ms-2">PRO <span class="text-gradient">x</span> Tech</span>
      </a>

      <!-- Toggle Button -->
      <button
          class="navbar-toggler border-0"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarNav"
      >
        <span class="navbar-toggler-icon"></span>
      </button>

      <!-- Links -->
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ms-auto fw-semibold">
          <li class="nav-item" v-for="link in links" :key="link.name">
            <a class="nav-link px-3" :href="link.href">
              {{ link.name }}
            </a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script setup>
const links = [
  { name: "About", href: "#about" },
  { name: "Services", href: "#services" },
  { name: "Portfolio", href: "#portfolio" },
  { name: "Contact", href: "#contact" },
]
</script>

<style scoped>
/* Custom gradient navbar */
.custom-navbar {
  background: rgba(15, 15, 30, 0.85);
  backdrop-filter: blur(10px);
  transition: background 0.3s ease-in-out;
}

/* Gradient accent */
.text-gradient {
  background: linear-gradient(45deg, #00d4ff, #ff007f);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

/* Navbar links */
.nav-link {
  color: #ddd !important;
  position: relative;
  transition: color 0.3s ease;
}

/* Hover underline animation */
.nav-link::after {
  content: "";
  position: absolute;
  width: 0%;
  height: 2px;
  bottom: 0;
  left: 50%;
  background: linear-gradient(45deg, #00d4ff, #ff007f);
  transition: all 0.3s ease;
}

.nav-link:hover {
  color: #fff !important;
}

.nav-link:hover::after {
  width: 100%;
  left: 0;
}

/* Active section (optional JS can update active) */
.nav-link.active {
  color: #fff !important;
}
.nav-link.active::after {
  width: 100%;
  left: 0;
}
</style>
