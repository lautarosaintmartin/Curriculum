<script>
    let oscuro = $state(false);

    if (
        typeof window !== "undefined" &&
        localStorage.getItem("oscuro") === "true"
    ) {
        oscuro = true;
        document.documentElement.classList.add("dark-mode");
    }

    function modoOscuro() {
        oscuro = !oscuro;

        document.documentElement.classList.toggle("dark-mode");
        localStorage.setItem("oscuro", oscuro);
    }
</script>

<button
    onclick={modoOscuro}
    class={oscuro
        ? "ml-auto bg-white border border-slate-200 px-4 py-2 rounded-full shadow-lg text-black"
        : "ml-auto bg-black border border-slate-200 px-4 py-2 rounded-full shadow-lg text-white"}
>
    {oscuro ? "☀︎" : "☾"}
</button>
