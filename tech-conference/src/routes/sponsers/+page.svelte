<script lang="ts">
  let sponsors = {
    gold: [
      { name: "TechCorp", logo: "/preview.jpg", link: "/preview.jpg" },
      { name: "Innovate Inc.", logo: "/preview2.jpg", link: "preview2.jpg" },
    ],
    silver: [
      { name: "Startup Hub", logo: "/preview3.jpg", link: "/preview3.jpg" },
    ],
    bronze: [
      { name: "Community Co.", logo: "/preview4.jpg", link: "/preview4.jpg" },
    ],
  };
</script>

<div class="sponsors-page">
  <h1 class="text-center">Our Sponsors</h1>
  <p class="text-center sponsors-description">
    We are proud to collaborate with these amazing organizations. Their support makes Tech Conference 2025 possible.
  </p>

  {#each Object.entries(sponsors) as [tier, sponsorsList]}
    <section class="sponsors-tier">
      <h2 class="tier-title">{tier.charAt(0).toUpperCase() + tier.slice(1)} Sponsors</h2>
      <div class="sponsors-grid">
        {#each sponsorsList as sponsor}
          <div class="sponsor-card">
            <a href={sponsor.link} target="_blank" rel="noopener noreferrer">
              <img src={sponsor.logo} alt={sponsor.name} class="sponsor-logo" />
              <p class="sponsor-name">{sponsor.name}</p>
            </a>
          </div>
        {/each}
      </div>
    </section>
  {/each}
</div>

<style>
/* Sponsors Page Style */
.sponsors-page {
  padding: 2rem 1rem;
  font-family: 'Roboto', sans-serif;
  background: linear-gradient(to bottom, #f8f9fa, #ffffff);
}

.sponsors-page h1 {
  font-size: 2.5rem;
  font-weight: bold;
  color: #2c3e50;
  margin-bottom: 1rem;
}

.sponsors-description {
  font-size: 1.1rem;
  color: #6c757d;
  margin-bottom: 2rem;
  text-align: center;
  max-width: 700px;
  margin-left: auto;
  margin-right: auto;
}

/* Tier Section */
.sponsors-tier {
  margin-bottom: 3rem;
}

.tier-title {
  font-size: 1.8rem;
  font-weight: bold;
  color: #333;
  text-align: center;
  margin-bottom: 1.5rem;
  text-transform: uppercase;
}

/* Sponsors Grid */
.sponsors-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  gap: 1.5rem;
  justify-items: center;
}

/* Sponsor Card */
.sponsor-card {
  text-align: center;
  background: white;
  padding: 1rem;
  border-radius: 10px;
  box-shadow: 0 8px 15px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.sponsor-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.15);
}

.sponsor-logo {
  width: 100px;
  height: auto;
  margin-bottom: 0.5rem;
}

.sponsor-name {
  font-size: 1rem;
  font-weight: bold;
  color: #333;
}

/* Responsive Design */
@media (max-width: 768px) {
  .sponsors-page h1 {
    font-size: 2rem;
  }

  .tier-title {
    font-size: 1.5rem;
  }

  .sponsors-description {
    font-size: 1rem;
  }

  .sponsors-grid {
    gap: 1rem;
  }
}
</style>
