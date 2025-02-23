<script lang="ts">
  export let sessions: { date: string; time: string; topic: string; speaker: string }[] = [];
</script>

<table class="schedule-table">
  <thead>
    <tr>
      <th>Date</th>
      <th>Time</th>
      <th>Topic</th>
      <th>Speaker</th>
    </tr>
  </thead>
  <tbody>
    {#each sessions as { date, time, topic, speaker }}
      <tr>
        <td>{date}</td>
        <td>{time}</td>
        <td>{topic}</td>
        <td>{speaker}</td>
      </tr>
    {/each}
  </tbody>
</table>
