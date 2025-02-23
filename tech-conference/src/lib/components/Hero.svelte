<script lang="ts">
  export let title: string = "Tech Conference 2025";
  export let tagline: string = "Shaping the Future of Technology";
  export let ctaText: string = "Learn More";
  export let ctaLink: string = "#";
</script>

<div class="hero">
  <h1>{title}</h1>
  <p>{tagline}</p>
  <a href={ctaLink} class="btn btn-light">{ctaText}</a>
</div>
