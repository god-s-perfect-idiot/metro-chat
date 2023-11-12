<script>
	import Button from '$lib/components/Button.svelte';
    import Loading from '$lib/components/Loading.svelte';
	import TextArea from '$lib/components/TextArea.svelte';
    $: messages = [
        {
            "msg": "Hello",
            "own": true
        },
        {
            "msg": "Hi",
            "own": false
        },
        {
            "msg": "How are you?",
            "own": true
        },
        {
            "msg": "I'm fine",
            "own": false
        },
        {
            "msg": "What about you?",
            "own": false
        },
        {
            "msg": "I'm fine too",
            "own": true
        },
        {
            "msg": "What are you doing?",
            "own": true
        },
        {
            "msg": "Nothing much",
            "own": false
        },
        {
            "msg": "Just chilling",
            "own": false
        },
        {
            "msg": "What about you?",
            "own": false
        },
        {
            "msg": "I'm just chilling too",
            "own": true
        },
        {
            "msg": "What do you do?",
            "own": true
        },
        {
            "msg": "I'm a student",
            "own": false
        },
        {
            "msg": "What about you?",
            "own": false
        },
        {
            "msg": "I'm a student too",
            "own": true
        },
        {
            "msg": "What do you study?",
            "own": true
        },
        {
            "msg": "I study computer science",
            "own": false
        },
        {
            "msg": "What about you?",
            "own": false
        },
        {
            "msg": "I study computer science too",
            "own": true
        },
        {
            "msg": "What do you do in your free time?",
            "own": true
        },
        {
            "msg": "I play games",
            "own": false
        },
        {
            "msg": "What about you?",
            "own": false
        },
        {
            "msg": "I play games too",
            "own": true
        },
        {
            "msg": "What games do you play?",
            "own": true
        },
        {
            "msg": "I play Valorant",
            "own": false
        },
        {
            "msg": "What about you?",
            "own": false
        },
        {
            "msg": "I play Valorant too",
            "own": true
        }
    ]
</script>

<div class="container">
    <div class="top-bar">
        <span>John Doe</span>
        <span class="age-sex">M 24</span>
    </div>
    <div class="messages">
        {#each messages as message}
            <div class={`message-holder ${message.own ? "end" : "start"}`}>
                {#if message.own}
                    <div class="own message">
                        {message.msg}
                    </div>
                {:else}
                    <div class="other message">
                        {message.msg}
                    </div>
                {/if}
            </div>
        {/each}
    </div>
    <div class="bottom-bar">
        <TextArea/>
        <div class="controls">
            <Button text="stop" action={() => {}}/>
            <Button text="send" action={() => {}}/>
        </div>
    </div>
</div>

<style>
    .end {
        justify-content: flex-end;
    }
    .start {
        justify-content: flex-start;
    }
    .message-holder {
        display: flex;
        width: 100%;
    }
    .message {
        display: flex;
        padding-top: 0.5rem;
        padding-bottom: 0.5rem;
        padding-left: 1rem;
        padding-right: 2rem;
        font-size: 1.1rem; 
        justify-content: flex-start;
    }
    .own {
        background-color: #707070;
        /* justify-self: flex-end; */
    }
    .other {
        background-color: #353535;
        /* justify-self: flex-start; */
    }
    .container {
        display: flex;
        flex-direction: column;
        padding: 1rem;
        height: calc(100vh - 3rem);
        gap: 2rem;
    }
    .top-bar {
        font-size: 1.4rem;
        display: flex;
        justify-content: space-between;
        align-items: center;
        font-weight: 300;
        height: 5%;
    }
    .messages {
        height: 85%;
        display: flex;
        overflow-y: scroll;
        flex-direction: column;
        gap: 1rem;
    }
    .bottom-bar {
        height: 25%;
        display: flex;
        flex-direction: column;
        gap: 2rem;
    }
    .controls {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    .age-sex {
        font-size: 1.3rem;
    }
</style>