<script>
  let ligada = false;

  function toggleLampada() {
    ligada = !ligada;
  }
</script>

<div class={`w-screen h-screen flex items-center justify-center transition-colors duration-1000 ${ligada ? 'bg-yellow-200 text-black' : 'bg-gray-900 text-white'}`}>
  <div class="text-center">
    <h1 class="text-2xl font-bold mb-6">Lâmpada Interativa</h1>
    <img
      src={ligada
        ? 'https://www.w3schools.com/js/pic_bulbon.gif'
        : 'https://www.w3schools.com/js/pic_bulboff.gif'}
      alt="Lâmpada"
      class="w-36 mx-auto mb-6"
    />
    <button
      on:click={toggleLampada}
      class={`px-6 py-2 text-lg rounded transition-colors duration-500 ${
        ligada ? 'bg-red-500 hover:bg-red-600 text-white' : 'bg-green-500 hover:bg-green-600 text-white'
      }`}
    >
      {ligada ? 'Apagar' : 'Acender'}
    </button>
  </div>
</div> 