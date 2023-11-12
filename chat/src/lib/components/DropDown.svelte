<script>
    export let options;
    $: isFocused = false;
    $: selected = options[0];
</script>

{#if isFocused}
    <div class="holder big"  on:click={() => isFocused = !isFocused} >
        {#each options as option}
            <span class="content" on:click={() => selected = option}>
                {option}
            </span>
        {/each}
    </div>
{:else}
    <div class="holder mini" on:click={() => isFocused = !isFocused}>
        {selected}
    </div>
{/if}


<style>
    .content {
        width: 100%;
    }
    .holder {
        font-size: 1.1rem;
        background-color: black;
        border: 2px solid white;
        padding-left: 1rem;
        display: flex;
        align-items: flex-start;
        color: white;
        flex-direction: column;
        justify-content: center;
        gap: 1rem;
    }
    .mini {
        height: 2rem;

    }
    .big {
        height: 5rem;
    }
</style>