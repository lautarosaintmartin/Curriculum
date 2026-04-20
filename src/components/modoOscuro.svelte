<script>
    let oscuro = $state(false);

    //typeof window !== undefined es para verificar que el codigo se este ejecutando en el navegador

    if (
        typeof window !== "undefined" &&
        localStorage.getItem("oscuro") === "true"
        //localStorage.getItem("oscuro") === "true" con esto verifico si el modo oscuro se uso anteriormente
    ) {
        oscuro = true;
        document.documentElement.classList.add("dark");
        //Agrega la clase dark al elemento html
    }

    function modoOscuro() {
        oscuro = !oscuro;

        document.documentElement.classList.toggle("dark");
        localStorage.setItem("oscuro", oscuro);
    }
</script>

<button
    onclick={modoOscuro}
    class={oscuro
        ? "ml-auto bg-white border border-slate-200 px-4 py-2 rounded-full shadow-lg text-slate-900"
        : "ml-auto bg-slate-900 border border-slate-200 px-4 py-2 rounded-full shadow-lg text-white"}
>
    {oscuro ? "☀︎" : "☾"}
</button>
