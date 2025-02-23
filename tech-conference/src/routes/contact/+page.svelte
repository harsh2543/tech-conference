<script lang="ts">
  let formData = { name: "", email: "", message: "" };

  function handleSubmit() {
    alert(`Thank you, ${formData.name}! Your message has been sent.`);
    formData = { name: "", email: "", message: "" }; // Reset form
  }
</script>

<div class="contact-page">
  <div class="container">
    <h1 class="text-center">Get in Touch</h1>
    <p class="text-center contact-description">
      Have a question or need assistance? Fill out the form below, and we'll get back to you shortly.
    </p>

    <form class="contact-form" on:submit|preventDefault={handleSubmit}>
      <div class="form-group">
        <label for="name">Your Name</label>
        <input
          type="text"
          id="name"
          class="form-control"
          bind:value={formData.name}
          placeholder="Enter your name"
          required
        />
      </div>

      <div class="form-group">
        <label for="email">Your Email</label>
        <input
          type="email"
          id="email"
          class="form-control"
          bind:value={formData.email}
          placeholder="Enter your email"
          required
        />
      </div>

      <div class="form-group">
        <label for="message">Your Message</label>
        <textarea
          id="message"
          class="form-control"
          bind:value={formData.message}
          rows="4"
          placeholder="Write your message here"
          required
        ></textarea>
      </div>

      <button type="submit" class="btn btn-primary">Send Message</button>
    </form>
  </div>
</div>

<style>
/* Contact Page Styles */
.contact-page {
  padding: 2rem 1rem;
  background: linear-gradient(to bottom, #f8f9fa, #ffffff);
}

.contact-page h1 {
  font-size: 2.5rem;
  font-weight: bold;
  margin-bottom: 1rem;
  color: #2c3e50;
}

.contact-description {
  font-size: 1.1rem;
  color: #6c757d;
  margin-bottom: 2rem;
  max-width: 600px;
  margin-left: auto;
  margin-right: auto;
}

/* Contact Form Styles */
.contact-form {
  background: white;
  padding: 2rem;
  border-radius: 15px;
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
  max-width: 600px;
  margin: 0 auto;
}

.contact-form .form-group {
  margin-bottom: 1.5rem;
}

.contact-form label {
  font-size: 0.9rem;
  font-weight: bold;
  margin-bottom: 0.5rem;
  display: block;
  color: #333;
}

.contact-form .form-control {
  width: 100%;
  padding: 0.75rem;
  border: 1px solid #ddd;
  border-radius: 10px;
  font-size: 1rem;
  transition: border-color 0.3s ease, box-shadow 0.3s ease;
}

.contact-form .form-control:focus {
  border-color: #007bff;
  box-shadow: 0 4px 10px rgba(0, 123, 255, 0.2);
  outline: none;
}

.contact-form button {
  display: block;
  width: 100%;
  padding: 0.85rem;
  font-size: 1.1rem;
  font-weight: bold;
  border-radius: 50px;
  border: none;
  background: linear-gradient(to right, #007bff, #0056b3);
  color: white;
  transition: all 0.3s ease;
  cursor: pointer;
}

.contact-form button:hover {
  background: linear-gradient(to right, #0056b3, #003a80);
  box-shadow: 0 8px 15px rgba(0, 91, 187, 0.3);
  transform: scale(1.05);
}

/* Media Queries for Responsiveness */
@media (max-width: 768px) {
  .contact-page h1 {
    font-size: 2rem;
  }

  .contact-form button {
    font-size: 1rem;
    padding: 0.75rem;
  }
}
</style>
