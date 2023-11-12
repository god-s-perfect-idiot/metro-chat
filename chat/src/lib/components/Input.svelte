<script>
    export let type;
</script>

<input type={type}/>

<style>
    input {
        width: calc(100% - 1rem);
        height: 2rem;
        background-color: #b9b9b9;
        font-size: 1.1rem;
        padding-left: 1rem;
    }
    input:active, input:focus, input:hover{
        background-color: white;
    }
</style>