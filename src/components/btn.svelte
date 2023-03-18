<script>
  let texto = "Texto inicial";
  let activo = false;

  function cambiarTexto() {
    activo = !activo;
    texto = activo ? "Texto aleatorio activado" : "Texto aleatorio desactivado";
  }
</script>

<div class="flex flex-col m-auto">
  <h1>{texto}</h1>
  <button on:click={cambiarTexto} class="bg-amber-700 text-white p-2 rounded-lg">
    {activo ? 'Desactivar' : 'Activar'} texto aleatorio
  </button>
  <a href="/" class="p-2 bg-amber-800 rounded-lg m-2 w-16 text-center text-white">Volver</a>
</div>
