<script lang="ts">
  export let src: string;
  export let alt = "Avatar picture";
</script>

<figure class="avatar">
  <img src={src} alt={alt} />
</figure>

<style>
  .avatar img {
    --size: 100px;
    width: var(--size);
    height: var(--size);
    border-radius: 50%;
    object-fit: cover;
  }
</style>
