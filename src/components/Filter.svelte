<script>
  import InputSearch from "./InputSearch.svelte";
  import Select from "./Select.svelte";
</script>

<style>
  .filter {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
</style>

<section class="filter">
  <InputSearch />
  <Select />
</section>
