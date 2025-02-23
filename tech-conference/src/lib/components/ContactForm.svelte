<script lang="ts">
  export let formData: { name: string; email: string; message: string } = {
    name: "",
    email: "",
    message: "",
  };

  export let handleSubmit: () => void;
</script>

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
