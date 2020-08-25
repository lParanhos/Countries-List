<script>
  export let country;
</script>

<style>
  li {
    width: 220px;
    height: 280px;
    border: 1px solid #e3e3e3;
  }

  .flag {
    width: 100%;
    height: 125px;
    object-fit: cover;
  }

  .info {
    padding: 15px;
    text-align: left;
  }
  .info > aside {
    padding-top: 10px;
    display: flex;
    flex-direction: column;
  }

  .info > aside span:not(:first-child) {
    margin-top: 5px;
  }
</style>

<li>
  <img src={country.flag} alt="flag" class="flag" />
  <section class="info">
    <h4>{country.name}</h4>
    <aside>
      <span>
        <strong>Population:</strong>
        {country.population}
      </span>
      <span>
        <strong>Region:</strong>
        {country.region}
      </span>
      <span>
        <strong>Capital:</strong>
        {country.capital}
      </span>
    </aside>
  </section>
</li>
