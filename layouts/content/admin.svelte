<script>
    import { authenticate } from '../cms/auth.svelte';
    const login = async () => {
        const authenticated = await authenticate();
        if (!authenticated) return;
    };
</script>

<button on:click={login}>Login</button>

<div>Go <a href="/">home</a></div>