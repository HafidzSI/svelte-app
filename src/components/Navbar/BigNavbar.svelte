<script>
    import CartButton from "../Cart/CartButton.svelte";
    import links from "../../constants/links";
    import {link} from "svelte-routing";
    import LoginLink from "../LoginLink.svelte";
</script>

<nav class="navbar">
    <div class="nav-container">
        <div class="nav-center">
            <!-- navlink -->
            <ul class="nav-links">
                {#each links as navlink}
                    <li>
                        <a href="{navlink.url}" use:link>{navlink.text}</a>
                    </li>
                {/each}            
            </ul>
            <!-- nav logo -->
            <a href="/" use:link class="nav-logo big-logo">
                <img src="/assets/images/logo.svg" class="logo" alt="razers logo">
            </a>
            <!-- cart toggle -->
            <div class="nav-aside">
                <LoginLink />
                <CartButton />
            </div>
        </div>
    </div>
</nav>