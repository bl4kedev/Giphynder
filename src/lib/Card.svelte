
<script>
    export let title;
    export let gifUrl;

    import { saveAs } from 'file-saver';

    const handleClick = () => {
        saveAs(gifUrl, 'giphynder.gif');
    }

</script>

<div class="
        card
        shadow-md
        shadow-gray-500
        w-full
        border
        border-gray-300
        mb-10
        overflow-hidden
        rounded-lg
        transition
        duration-200
        hover:ease-linear
        hover:scale-105
    ">


    <img class="w-full max-h-44" 
            src={gifUrl}
            alt="">
    
    <div class="
        flex
        flex-col
        items-center
        justify-around
        p-2
    ">
        <p class="p-5 text-center"> { title } </p>
        <button class="
            bg-orange-500
            text-white
            py-2
            px-6
            rounded-md
            mb-3
        "
            on:click={handleClick}
        >Descargar</button>
    </div>

</div>