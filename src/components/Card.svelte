<script lang="ts">
  export let url: string;
  export let title: string;
</script>

<li class="card-container">
  <a href={url} target="_blank">
    <div class="card">
      <h3>{title}</h3>
    </div>
  </a>
</li>

<style>
  .card-container {
    width: 100%;
    margin-bottom: 1.5rem;
  }

  .card-container:last-child {
    margin-bottom: 0;
  }

  .card {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    border: 2px solid var(--light);
    color: var(--light);
    border-radius: 8px;
    padding: 1.5rem;
  }

  .card:hover {
    background-color: var(--light);
    color: var(--dark);
  }

  h3 {
    font-size: 2.2rem;
    font-weight: 600;
    text-align: center;
  }
</style>
