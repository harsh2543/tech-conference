<script lang="ts">
  let speakers = [
    {
      name: "Jane Doe",
      title: "CTO, TechCorp",
      bio: "Pioneer in AI and Machine Learning, dedicated to driving technological innovation.",
      image: "/bestman_807609.png",
    },
    {
      name: "John Smith",
      title: "Blockchain Expert",
      bio: "Renowned expert in blockchain technology and decentralized applications.",
      image: "/bestman_807711.png",
    },
    {
      name: "Emily Davis",
      title: "Cybersecurity Specialist",
      bio: "Leader in data privacy and cybersecurity, ensuring secure digital environments.",
      image: "/manager_1010829.png",
    },
  ];
</script>

<div class="speakers-page">
  <h1 class="text-center">Meet the Speakers</h1>
  <p class="text-center speakers-description">
    Get inspired by industry leaders who are shaping the future of technology. Explore their expertise and stories.
  </p>

  <div class="speakers-grid">
    {#each speakers as speaker}
      <div class="speaker-card">
        <img src={speaker.image} alt={speaker.name} class="speaker-image" />
        <div class="speaker-details">
          <h3 class="speaker-name">{speaker.name}</h3>
          <p class="speaker-title">{speaker.title}</p>
          <p class="speaker-bio">{speaker.bio}</p>
        </div>
      </div>
    {/each}
  </div>
</div>

<style>
/* Speakers Page Styles */
.speakers-page {
  padding: 2rem 1rem;
  font-family: 'Roboto', sans-serif;
  background: linear-gradient(to bottom, #f8f9fa, #ffffff);
}

.speakers-page h1 {
  font-size: 2.5rem;
  font-weight: bold;
  color: #2c3e50;
  margin-bottom: 1rem;
}

.speakers-description {
  font-size: 1.1rem;
  color: #6c757d;
  margin-bottom: 2rem;
  text-align: center;
  max-width: 700px;
  margin-left: auto;
  margin-right: auto;
}

/* Speakers Grid */
.speakers-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
  justify-items: center;
}

/* Speaker Card */
.speaker-card {
  text-align: center;
  background: white;
  border-radius: 15px;
  padding: 1.5rem;
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  max-width: 300px;
}

.speaker-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
}

/* Speaker Image */
.speaker-image {
  width: 100%;
  height: 200px;
  object-fit: cover;
  border-radius: 10px;
  margin-bottom: 1rem;
}

/* Speaker Details */
.speaker-details {
  padding: 1rem 0;
}

.speaker-name {
  font-size: 1.25rem;
  font-weight: bold;
  color: #2c3e50;
  margin-bottom: 0.5rem;
}

.speaker-title {
  font-size: 1rem;
  font-weight: 600;
  color: #007bff;
  margin-bottom: 0.5rem;
}

.speaker-bio {
  font-size: 0.9rem;
  color: #6c757d;
  line-height: 1.5;
}

/* Responsive Design */
@media (max-width: 768px) {
  .speakers-page h1 {
    font-size: 2rem;
  }

  .speakers-description {
    font-size: 1rem;
  }

  .speaker-card {
    padding: 1rem;
  }
}
</style>
