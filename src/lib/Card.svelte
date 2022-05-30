
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
        overflow-hidden
        rounded-lg
    ">

    <img class="w-full max-h-44" 
         src={gif.images["fixed_height"].url}
         alt="">
    <div class="
        flex
        flex-col
        items-center
        justify-around
        p-2
    ">
        <p class="p-5 text-center"> { gif["title"] } </p>
        <button class="
            bg-orange-500
            text-white
            py-2
            px-6
            rounded-md
            mb-3
        ">Descargar</button>
    </div>

</div>