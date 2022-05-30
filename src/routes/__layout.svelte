<script>
    import "../app.css";
</script>


<header class="
        bg-slate-600
    ">
    <div class="
        container
        w-10/12
        mx-auto
        p-4
        ">
        <h1 class="
            text-white
            text-3xl
            font-bold
            text-center
        ">GIPHYNDER</h1>
    </div>
</header>
<main>
    <slot></slot>
</main>
<footer class="
        bg-slate-900
        text-white
        text-center
        py-2
        w-full
        left-0
        bottom-0
        fixed
    ">
    <p>Creado por Manuel Berganza</p>
</footer>