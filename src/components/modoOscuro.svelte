<script>
    let oscuro = $state(false)

    function modoOscuro(){
        oscuro = !oscuro
        document.documentElement.classList.toggle('dark')
    }
</script>

<button 
    onclick={modoOscuro}
    class= "fixed bottom-6 right-6">

    {oscuro ? '☀️ Modo claro' : '🌙 Modo oscuro'}
</button>