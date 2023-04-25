<script>
    import App from "../components/App.svelte";

    let name = 'SvelteKit'
    setTimeout(() => { name = 'Darío' }, 2000)
</script>
<App />