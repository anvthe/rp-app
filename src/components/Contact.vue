<template>
  <section id="contact" class="py-5 bg-light position-relative">
    <div class="container">
      <h2 class="text-center mb-5 fw-bold display-5 text-gradient">Get In Touch</h2>

      <div class="row justify-content-center">
        <div class="col-lg-8">
          <div class="card shadow-lg border-0 rounded-4 p-4 contact-card">
            <form class="p-3">
              <div class="mb-3">
                <input
                    type="text"
                    class="form-control form-control-lg stylish-input"
                    placeholder="Your Name"
                    required
                />
              </div>
              <div class="mb-3">
                <input
                    type="email"
                    class="form-control form-control-lg stylish-input"
                    placeholder="Your Email"
                    required
                />
              </div>
              <div class="mb-3">
                <textarea
                    class="form-control form-control-lg stylish-input"
                    rows="5"
                    placeholder="Your Message"
                    required
                ></textarea>
              </div>
              <button type="submit" class="btn btn-gradient btn-lg w-100">
                🚀 Send Message
              </button>
            </form>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
/* Gradient title */
.text-gradient {
  background: linear-gradient(45deg, #007bff, #6610f2);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

/* Contact card */
.contact-card {
  background: rgba(255, 255, 255, 0.9);
  backdrop-filter: blur(12px);
  border: 1px solid rgba(255, 255, 255, 0.25);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}
.contact-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 12px 32px rgba(0, 0, 0, 0.15);
}

/* Input fields */
.stylish-input {
  border-radius: 12px;
  border: 1px solid #ddd;
  padding: 14px 18px;
  transition: all 0.3s ease;
}
.stylish-input:focus {
  border-color: #007bff;
  box-shadow: 0 0 12px rgba(0, 123, 255, 0.25);
  outline: none;
}

/* Gradient button */
.btn-gradient {
  background: linear-gradient(45deg, #007bff, #6610f2);
  border: none;
  border-radius: 12px;
  color: #fff;
  font-weight: 600;
  transition: all 0.3s ease;
}
.btn-gradient:hover {
  background: linear-gradient(45deg, #6610f2, #007bff);
  transform: scale(1.02);
  box-shadow: 0 8px 20px rgba(0, 123, 255, 0.25);
}
</style>
