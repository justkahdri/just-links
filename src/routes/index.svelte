<script lang="ts">
  import Card from '../components/Card.svelte';
  import Avatar from '../components/Avatar.svelte';

  let links = [["https://example.com", "Visita nuestro Ejemplo"], ["https://http.cat", "GATITOS GATITOS GATITOS"]];
  const title = "Rich Harris";
</script>

<main>
  <Avatar src="https://pbs.twimg.com/profile_images/557940120184041473/bFyXy8Pu_400x400.jpeg" alt={title} />
  <h1>{title}</h1>
  <ul class="links-list">
    {#each links as [url, title]}
      <Card {url} {title}/>
    {/each}
  </ul>
</main>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Source+Sans+Pro:ital,wght@0,300;0,400;0,600;0,700;1,300;1,400;1,600&display=swap');

  /* GLOBALS */
  :global(*) {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  :global(:root) {
    font-size: 62.5%;
    font-family: 'Source Sans Pro', sans-serif;

    --dark: #2e2e2e;
    --light: azure;
  }

  :global(body) {
    color: white;
    min-height: 100vh;
    background: linear-gradient(90deg, hsla(276, 91%, 79%, 1) 0%, hsla(254, 74%, 65%, 1) 100%);
  }

  :global(body), main {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  :global(a) {
    text-decoration: none;
  }

  /* MAIN STYLES */
  main {
    width: 100%;
    padding: 0 1rem;
  }

  h1 {
    font-size: 1.8rem;
    margin-top: 0.8rem;
    margin-bottom: 3rem;
  }

  ul.links-list {
    width: 100%;
    min-height: 60vh;
    overflow-y: auto;
  }

</style>
