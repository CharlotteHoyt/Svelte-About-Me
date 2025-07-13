<!-- src/lib/ImageCard.svelte -->

<script>
  export let image;  // Image URL prop
  export let title;  // Title prop
  export let description;  // Description prop
</script>

<style>
  .card {
    background-color: #FFDEDE;
    border-radius: 10px;
    overflow: hidden;
    margin: 20px;
    text-align: center;
    width: 250px;
    height: 325px;
    overflow-y: auto;
  }

  .card h2 {
    color: #FF8551;
    font-weight: bold;
    font-size: 1.25em;
  }

  .card p {
    color: #6A6767;
  }

  .card img {
    width: 100%;
    height: auto;
    border-radius: 10px;
  }

  .card * {
    background-color: #FFDEDE;
  }

  /*.card-content {
    padding: 15px;
  }*/

  .card-title {
    font-size: 1.5em;
    color: #333;
    margin: 0 0 10px 0;
  }

  .card-description {
    margin: 0;
  }
</style>

<div class="card">
  <img src={image} alt={title} />
  <div class="card-content">
    <h2 class="card-title">{title}</h2>
    <p class="card-description">{description}</p>
  </div>
</div>
