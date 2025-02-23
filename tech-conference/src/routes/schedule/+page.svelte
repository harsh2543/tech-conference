<script lang="ts">
  let sessions = [
    { date: "24-Feb-2025", time: "10:00 AM", topic: "Future of AI", speaker: "Jane Doe" },
    { date: "24-Feb-2025", time: "12:00 PM", topic: "Blockchain Revolution", speaker: "John Smith" },
    { date: "25-Feb-2025", time: "02:00 PM", topic: "Cybersecurity Trends", speaker: "Emily Davis" },
  ];
</script>

<div class="schedule-page">
  <h1 class="text-center">Conference Schedule</h1>
  <p class="text-center schedule-description">
    Discover the exciting lineup of sessions, keynotes, and discussions. Plan your day and make the most of Tech Conference 2025.
  </p>

  <div class="schedule-table-container">
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
        {#each sessions as session}
          <tr>
            <td>{session.date}</td>
            <td>{session.time}</td>
            <td>{session.topic}</td>
            <td>{session.speaker}</td>
          </tr>
        {/each}
      </tbody>
    </table>
  </div>
</div>

<style>
/* Schedule Page Styles */
.schedule-page {
  padding: 2rem 1rem;
  font-family: 'Roboto', sans-serif;
  background: linear-gradient(to bottom, #f8f9fa, #ffffff);
}

.schedule-page h1 {
  font-size: 2.5rem;
  font-weight: bold;
  color: #2c3e50;
  margin-bottom: 1rem;
}

.schedule-description {
  font-size: 1.1rem;
  color: #6c757d;
  margin-bottom: 2rem;
  text-align: center;
  max-width: 700px;
  margin-left: auto;
  margin-right: auto;
}

/* Table Styles */
.schedule-table-container {
  overflow-x: auto; /* Allow horizontal scrolling for smaller screens */
  margin-top: 1.5rem;
  border-radius: 15px;
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
  background-color: white;
}

.schedule-table {
  width: 100%;
  border-collapse: collapse;
  background-color: white;
  border-radius: 15px;
  overflow: hidden;
}

.schedule-table th {
  background-color: #007bff;
  color: white;
  text-transform: uppercase;
  font-size: 0.9rem;
  font-weight: bold;
  padding: 1rem;
  text-align: left;
  border-bottom: 3px solid #0056b3;
}

.schedule-table td {
  padding: 1rem;
  color: #555;
  border: 1px solid #dee2e6;
}

.schedule-table tr:nth-child(even) {
  background-color: #f9f9f9;
}

.schedule-table tr:hover {
  background-color: #e9f5ff;
  transition: background-color 0.3s ease;
}

/* Responsive Design */
@media (max-width: 768px) {
  .schedule-page h1 {
    font-size: 2rem;
  }

  .schedule-description {
    font-size: 1rem;
  }

  .schedule-table th, .schedule-table td {
    font-size: 0.9rem;
    padding: 0.75rem;
  }
}
</style>
