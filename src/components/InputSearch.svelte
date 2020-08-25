<script>
  import Icon from "svelte-awesome";
  import { search } from "svelte-awesome/icons";
</script>

<style>
  div {
    position: relative;
    margin: 0;
    max-width: 350px;
    height: 40px;
  }

  input {
    padding: 0;
    padding-left: 50px;
    margin: 0;
    height: 40px;
    width: 350px;
  }
</style>

<div style="margin: 0;">
  <Icon style="position: absolute; bottom:30%" data={search} scale={1.3} />
  <input placeholder="Search for a country..." />
</div>
