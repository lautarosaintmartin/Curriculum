<script>
    let oscuro = $state(false)

    if(typeof window !== 'undefined' && localStorage.getItem('oscuro') === 'true'){
        oscuro = true
        document.documentElement.classList.add('dark-mode')
    }

    function modoOscuro(){
        oscuro = !oscuro
       
        document.documentElement.classList.toggle('dark-mode')
        localStorage.setItem('oscuro', oscuro)
    }
</script>

<button 
    onclick={modoOscuro}
    class= {oscuro ? "fixed bottom-6 right-6 bg-black border border-slate-200 px-4 py-2 rounded-full shadow-lg text-white" : "fixed bottom-6 right-6 bg-black border border-slate-200 px-4 py-2 rounded-full shadow-lg text-white"}>
    
    {oscuro ? 'Modo claro' : 'Modo oscuro'}
</button>