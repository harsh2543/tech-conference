<script lang="ts">
  export let name: string;
  export let title: string;
  export let bio: string;
  export let image: string;
</script>

<div class="card">
  <img src={image} alt={name} class="card-img-top" />
  <div class="card-body">
    <h5 class="card-title">{name}</h5>
    <p class="card-text">{title}</p>
    <p class="card-bio">{bio}</p>
  </div>
</div>
