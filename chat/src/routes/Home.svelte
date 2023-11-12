<script>
	import Button from "$lib/components/Button.svelte";
import DropDown from "$lib/components/DropDown.svelte";
import Input from "$lib/components/Input.svelte";

</script>
<div class="container">
    <span>METRO CHAT</span>
    <span class="title">chat</span>
    <span class="hero">Get started with Metro Chat. It is simple, easy to use and a lot of fun! No sign up required. No personal data collection. Here's 2013!</span>
    <div class="form">
        <div class="form-row">
            <label>Name</label>
            <Input type="text" />
        </div>
        <div class="form-row">
            <label>Age</label>
            <Input type="number" />
        </div>
        <div class="form-row">
            <label>Sex</label>
            <DropDown options={["male", "female"]} />
        </div>
    </div>
    <div class="action">
        <Button text="start" action={() => {}}/>
    </div>
</div>

<style>
    .action {
        margin-top: 5rem;
    }
    .container {
        display: flex;
        flex-direction: column;
        padding: 1rem;
    }
    .title {
        font-size: 4rem;
        font-weight: 300;
    }
    .hero {
        font-size: 1rem;
        font-weight: 300;
        margin-top:2rem;
        color: #A0A0A0;
    }
    label {
        color: #A0A0A0;
        font-size: 1rem;
    }
    .form {
        margin-top: 5rem;
        display: flex;
        flex-direction: column;
        gap: 1rem;
    }
    .form-row {
        display: flex;
        flex-direction: column;
        gap: 1rem;
    }
</style>