
<script>

    // export let title = '';
    export let gif;
    // console.log(gif.images.downsized.url);

</script>

<div class="
        card
        shadow-xl
        w-full
        border
        mb-10
    ">

    <img class="w-full" 
         src={gif.images.downsized.url}
         alt="">
    <div class="
        flex
        flex-col
        items-center
        justify-around
        p-4
    ">
        <p> { gif["title"] } </p>
        <button class="
            bg-orange-700
            text-white
            py-2
            px-6
        ">Descargar</button>
    </div>

</div>