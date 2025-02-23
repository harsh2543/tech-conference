<script>
  const highlights = [
    "Keynote speeches from industry leaders",
    "Panels on emerging tech trends",
    "Networking opportunities with experts",
    "Hands-on workshops and live demos"
  ];
</script>

<div class="about-page">
  <section class="hero-section">
    <h1>About Tech Conference 2025</h1>
    <p>
      Join us at Tech Conference 2025, where innovation meets collaboration. Discover the future of technology with the brightest minds in the industry.
    </p>
  </section>

  <section class="about-content">
    <h2>Our Mission</h2>
    <p>
      Our mission is to foster innovation and collaboration within the tech community by bringing together leaders, startups, and enthusiasts.
    </p>

    <h2>What to Expect</h2>
    <ul class="highlights">
      {#each highlights as item}
        <li>✅ {item}</li>
      {/each}
    </ul>

    <div class="cta-section">
      <h3>Join Us!</h3>
      <p>Be part of a transformative experience. Don’t miss this opportunity to shape the future of technology.</p>
      <button class="btn btn-primary">Register Now</button>
    </div>
  </section>
</div>

<style>
/* About Page Styles */
.about-page {
  padding: 2rem 1rem;
  font-family: 'Roboto', sans-serif;
  background: linear-gradient(to bottom, #f8f9fa, #ffffff);
}

/* Hero Section */
.hero-section {
  background: linear-gradient(to right, #007bff, #0056b3);
  color: white;
  text-align: center;
  padding: 3rem 2rem;
  border-radius: 15px;
  margin-bottom: 2rem;
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
}

.hero-section h1 {
  font-size: 2.5rem;
  font-weight: bold;
  margin-bottom: 1rem;
}

.hero-section p {
  font-size: 1.25rem;
  color: #dbeafe;
}

/* About Content */
.about-content {
  max-width: 800px;
  margin: 0 auto;
  padding: 2rem;
  background: white;
  border-radius: 15px;
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
}

.about-content h2 {
  font-size: 1.8rem;
  font-weight: bold;
  color: #333;
  margin-bottom: 1rem;
}

.about-content p {
  font-size: 1rem;
  color: #6c757d;
  margin-bottom: 2rem;
}

/* Highlights */
.highlights {
  list-style: none;
  padding: 0;
  margin: 0;
}

.highlights li {
  font-size: 1rem;
  margin-bottom: 1rem;
  color: #333;
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.highlights li::before {
  content: '✅';
  color: #007bff;
  font-size: 1.2rem;
}

/* Call-to-Action Section */
.cta-section {
  text-align: center;
  margin-top: 2rem;
}

.cta-section h3 {
  font-size: 1.5rem;
  color: #333;
  font-weight: bold;
  margin-bottom: 0.5rem;
}

.cta-section p {
  font-size: 1rem;
  color: #6c757d;
  margin-bottom: 1rem;
}

.cta-section .btn {
  padding: 0.75rem 1.5rem;
  font-size: 1rem;
  font-weight: bold;
  border-radius: 50px;
  background: linear-gradient(to right, #007bff, #0056b3);
  color: white;
  border: none;
  transition: all 0.3s ease-in-out;
}

.cta-section .btn:hover {
  background: linear-gradient(to right, #0056b3, #003a80);
  box-shadow: 0 8px 15px rgba(0, 91, 187, 0.3);
  transform: scale(1.05);
}

/* Responsive Design */
@media (max-width: 768px) {
  .hero-section h1 {
    font-size: 2rem;
  }

  .hero-section p {
    font-size: 1rem;
  }

  .about-content {
    padding: 1.5rem;
  }
}
</style>
