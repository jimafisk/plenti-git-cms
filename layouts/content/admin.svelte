<script>
    import { authenticate } from '../cms/auth.svelte';

    let loggedIn = false;
    const login = async () => {
        const authenticated = await authenticate();
        if (authenticated) {
            loggedIn = true;
        }
    };
</script>

{#if loggedIn}
    <h1>Welcome!</h1>
{:else}
    <button on:click={login}>Login</button>
{/if}

<div>Go <a href="/">home</a></div>