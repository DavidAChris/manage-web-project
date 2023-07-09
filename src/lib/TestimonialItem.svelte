<script>
    export let personName;
    export let quote;
    export let personImg;
    export let alt = '';
    export let first = false;
</script>

{#if first}
    <div class="flex flex-col items-center p-6 space-y-6 rounded-lg bg-veryLightGray md:w-1/3">
        <img src={personImg}
             alt={alt} class="w-16 -mt-14">
        <h5 class="text-lg font-bold">{personName}</h5>
        <p class="text-sm text-darkGrayishBlue">
            "{quote}"
        </p>
    </div>
{:else }
    <div class="hidden md:flex flex-col items-center p-6 space-y-6 rounded-lg bg-veryLightGray md:w-1/3">
        <img src={personImg} alt={alt} class="w-16 -mt-14">
        <h5 class="text-lg font-bold">{personName}</h5>
        <p class="text-sm text-darkGrayishBlue">
            "{quote}"
        </p>
    </div>
{/if}