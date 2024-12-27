<script>
    import Navbar from './lib/components/Navbar.svelte';
    import Inicio from './lib/components/Inicio.svelte';
    import AcercaDe from './lib/components/AcercaDe.svelte';
    import Contacto from './lib/components/Contacto.svelte';
</script>

<Navbar />

<div class="content">
    <Inicio class="section" />
    <AcercaDe class="section" />
    <Contacto class="section" />
</div>

<style>
    .content {
        padding-top: 70px; /* Espacio para el navbar fijo */
    }
</style>
