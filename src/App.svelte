<script>
  import { onMount } from "svelte";

  import Card from "./components/Card.svelte";
  import Filter from "./components/Filter.svelte";
  import Header from "./components/Header.svelte";

  export let countries = [];

  onMount(async () => {
    const res = await fetch("https://restcountries.eu/rest/v2/region/europe");
    countries = await res.json();
  });
</script>

<style>
  main {
    text-align: center;
    max-width: 240px;
    margin: 0;
    padding: 0;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }

  .body {
    padding: 30px 30px;
  }

  ul {
    list-style: none;
    display: flex;
    flex-wrap: wrap;
  }
</style>

<main>
  <Header />
  <section class="body">
    <Filter />
    <ul class="countryList">
      {#each countries as country}
        <Card {country} />
      {:else}
        <span>Loading ...</span>
      {/each}
    </ul>
  </section>
</main>
