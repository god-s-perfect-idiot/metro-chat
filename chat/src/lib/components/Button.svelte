<script>
    export let action;
    export let text;
</script>

<span on:click={() => {action()}}>
    {text}
</span>

<style>
    span {
        height: 2rem;
        font-size: 1.1rem;
        background-color: black;
        color: white;
        border: 2px solid white;
        width: fit-content;
        padding-left: 3rem;
        padding-right: 3rem;
        padding-top: 0.25rem;
        padding-bottom: 0.25rem;
        display: flex;
        justify-content: center;
        align-items: center;
    }
</style>