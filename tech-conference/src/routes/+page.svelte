<script lang="ts">
  let keynoteSpeakers = [
    { name: "Jane Doe", title: "CTO, TechCorp", image: "/bestman_807609.png" },
    { name: "John Smith", title: "Blockchain Expert", image: "/bestman_807711.png" },
    { name: "Emily Davis", title: "Cybersecurity Specialist", image: "/manager_1010829.png" },
  ];
</script>

<div class="home-page">
  <!-- Hero Section -->
  <div class="hero">
    <h1>Tech Conference 2025</h1>
    <p>Shaping the Future of Technology</p>
    <button class="btn btn-light">Learn More</button>
  </div>

  <!-- Welcome Section -->
  <div class="welcome-section">
    <h2>Welcome to Tech Conference 2025</h2>
    <p>
      Join the brightest minds in technology for a two-day event packed with inspiring keynotes, discussions, and networking.
    </p>
  </div>

  <!-- Keynote Speakers Section -->
  <section class="keynote-section">
    <h3>Keynote Speakers</h3>
    <div class="keynote-grid">
      {#each keynoteSpeakers as speaker}
        <div class="card">
          <img src={speaker.image} alt="{speaker.name}" class="card-img-top" />
          <div class="card-body">
            <h5 class="card-title">{speaker.name}</h5>
            <p class="card-text">{speaker.title}</p>
          </div>
        </div>
      {/each}
    </div>
  </section>

  <!-- Register Section -->
  <div class="register-section">
    <h3>Don't Miss Out!</h3>
    <p>Be part of the conversation shaping tomorrow's technologies. Register now to secure your spot.</p>
    <button class="btn btn-primary">Register Now</button>
  </div>
</div>

<style>
/* Home Page Styles */
.home-page {
  padding: 2rem 1rem;
}

/* Hero Section */
.hero {
  background: linear-gradient(to right, #007bff, #0056b3);
  color: white;
  text-align: center;
  padding: 4rem 2rem;
  border-radius: 15px;
  box-shadow: 0 8px 15px rgba(0, 0, 0, 0.2);
  margin-bottom: 2rem;
}

.hero h1 {
  font-size: 3rem;
  font-weight: bold;
  margin-bottom: 1rem;
}

.hero p {
  font-size: 1.25rem;
  margin-bottom: 2rem;
  color: #fff;
}

.hero .btn {
  padding: 0.85rem 2rem;
  font-size: 1.25rem;
  font-weight: bold;
  transition: all 0.3s ease-in-out;
}

.hero .btn:hover {
  background: linear-gradient(to right, #007bff, #0056b3);
  color: white;
}

/* Welcome Section */
.welcome-section {
  text-align: center;
  background-color: #ffffff;
  padding: 2rem;
  border-radius: 15px;
  box-shadow: 0 8px 15px rgba(0, 0, 0, 0.1);
  margin-bottom: 2rem;
}

.welcome-section h2 {
  font-size: 2rem;
  font-weight: bold;
  color: #2c3e50;
  margin-bottom: 1rem;
}

.welcome-section p {
  font-size: 1rem;
  color: #555;
}

/* Keynote Section */
.keynote-section h3 {
  font-size: 1.8rem;
  font-weight: bold;
  color: #2c3e50;
  margin-bottom: 2rem;
  text-align: center;
}

.keynote-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 1.5rem;
}

/* Register Section */
.register-section {
  background: linear-gradient(to right, #007bff, #0056b3);
  color: white;
  text-align: center;
  padding: 2rem 1rem;
  border-radius: 15px;
  box-shadow: 0 8px 15px rgba(0, 0, 0, 0.2);
  margin-top: 2rem;
}

.register-section h3 {
  font-size: 1.5rem;
  font-weight: bold;
  margin-bottom: 1rem;
}

.register-section p {
  font-size: 1rem;
  margin-bottom: 1.5rem;
  color: #fff;
}

.register-section .btn {
  background: #fff;
  color: #0056b3;
  padding: 0.75rem 1.5rem;
  font-size: 1rem;
  font-weight: bold;
  transition: all 0.3s ease-in-out;
}

.register-section .btn:hover {
  background: linear-gradient(to right, #007bff, #0056b3);
  color: #fff;
}
</style>
