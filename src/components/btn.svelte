<script>
    let texto = "Texto inicial";
    
    function cambiarTexto() {
      texto = "Texto aleatorio "
    }
  </script>
  
  <div class="flex flex-col m-auto">
  <h1>{texto}</h1>

    <button on:click={cambiarTexto} class="bg-amber-700 text-white p-2 rounded-lg">Cambiar texto</button>
  </div>
