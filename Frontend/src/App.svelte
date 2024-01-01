<script>
    import Router from "svelte-spa-router"
    import SignUp from './routes/SignUp.svelte'
    import Login from './routes/Login.svelte'

    const routes = {
        '/': SignUp,
        '/Login': Login,
    }
</script>