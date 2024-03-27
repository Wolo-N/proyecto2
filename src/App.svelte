<script>
  let valores = [10, 25, 33, 62, 75, 100]
  let numeros = [];

  for (let i = 1; i <= 100; i++) {
    numeros.push(i);
  }
</script>

<main>
  <h1>MUERTES POR COVID-19 
    CADA 100 CONTAGIADOS</h1>


  <div id="BANDERAS">
    <img class="flag" src="./images/ISRAEL.png" alt="ISRAEL">
    <img class="flag" src="./images/ESTADOS UNIDOS.png" alt="ESTADOS UNIDOS">
    <img class="flag" src="./images/BRASIL.png" alt="BRASIL">
    <img class="flag" src="./images/ARGENTINA.png" alt="ARGENTINA">
    <img class="flag" src="./images/INDIA.png" alt="INDIA">
    <img class="flag" src="./images/CHINA.png" alt="CHINA">
  </div>

  <div id="GRAFICOS">
    {#each valores as n}
    <div id="PAISES">
      {#each numeros as i}
          {#if i <= n}
          <img class="ataudes" src="./images/ataud.png" alt="ataud"/>

        {:else}
          <img class="personas" src="./images/PERSONA.png" alt="PERSONA"/>
          {/if}
      {/each}
    </div>
    {/each}
  </div>
</main>

<style>
  :global(body){
    background-color: #1F2229;
  }


  h1{
    font-family: 'Merriweather';
    font-weight: 300;
    color: white;
  }

  #BANDERAS{
    display: flex;
    flex-direction: row;
    justify-content:space-around;
  }

  .flag{
    height: 170px;
    width: 170px;
  }

  .ataudes, .personas{
    height: 20px;
    width: 20px;
  }

  #PAISES{
    height: 200px;
    width: 200px;
    display: block;
  }

  #GRAFICOS{
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
  }
</style>
