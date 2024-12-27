<script>
    import { Router, Route, Link } from "svelte-routing";
    import Inicio from './Inicio.svelte';
    import AcercaDe from './AcercaDe.svelte';
    import Contacto from './Contacto.svelte';
</script>

<Router>
    <nav>
        <div class="nav-container">
            <!-- Ruta relativa a la raíz para la imagen -->
            <img src="/logo.png" alt="Logo" class="logo" />
            <ul>
                <li>
                    <Link to="/">Inicio</Link>
                </li>
                <li>
                    <Link to="/acerca">Acerca De</Link>
                </li>
                <li>
                    <Link to="/contacto">Contacto</Link>
                </li>
            </ul>
        </div>
    </nav>

    <!-- Definición de las rutas -->
    <Route path="/"><Inicio /></Route>
    <Route path="/acerca"><AcercaDe /></Route>
    <Route path="/contacto"><Contacto /></Route>
</Router>

<style>
    nav {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        background-color: white; /* Fondo oscuro */
        box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        z-index: 100;
        padding: 10px;
        color: black; /* Color de texto blanco para contraste */
    }

    .nav-container {
        display: flex;
        justify-content: space-between;
        align-items: center;
        max-width: 960px;
        margin: 0 auto;
        padding: 0 20px;
    }

    .logo {
        max-height: 50px;
        vertical-align: middle;
        margin-right: 20px;
    }

    nav ul {
        list-style: none;
        padding: 0;
        margin: 0;
        display: flex;
        gap: 20px;
    }

    nav li {
        margin: 0;
    }

    /* Estilos para enlaces */
   

    /* Estilos móviles */
    @media (max-width: 768px) {
        .nav-container {
            flex-direction: column;
            align-items: flex-start;
        }

        nav ul {
            flex-direction: column;
            align-items: flex-start;
            margin-top: 10px;
        }

        .logo {
            margin: 0px;
            margin-bottom: 10px;
        }

        nav li {
            margin-bottom: 10px;
        }
    }
</style>
