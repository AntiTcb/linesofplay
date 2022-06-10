<script>
    import 'carbon-components-svelte/css/g80.css'
    import '../app.scss'
    import Header from '$components/Header.svelte'
    import Footer from '$components/Footer.svelte'
    import { Content } from 'carbon-components-svelte'
</script>

<svelte:head>
    <title>Lines of Play</title>
</svelte:head>

<Header />
<Content>
    <slot />
</Content>
<Footer />
