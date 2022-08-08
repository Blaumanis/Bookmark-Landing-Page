<script>
    import SmallNavbar from "./SmallNavbar.svelte";
    import {slide} from 'svelte/transition';
    let open = false;

    function showMenu() {
        open = true;
    }

</script>

{#if open}
     <SmallNavbar {open} />
{:else}
<nav transition:slide>
    <a href="#" class="logo"><img class="logo-img" src="../images/logo-bookmark.svg" alt="logo"></a>
    <ul>
        <li><a href="#">features</a></li>
        <li><a href="#">pricing</a></li>
        <li><a href="#">contact</a></li>
        <li class="active"><a href="#">login</a></li>
    </ul>
    <img on:click={showMenu} class="hamburger-btn" src="../images/icon-hamburger.svg" alt="hamburger-icon">
</nav>
{/if}


<style>
    nav {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 2rem 0;
    }
    .logo {
        padding-left: 2.5rem;
    }
    .logo-img {
        width: 175px;
    }
    ul {
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 0 2rem;
    }
    ul li {
        padding: 0 1rem;
    }
    li a {
        text-transform: uppercase;
        color: var(--veryDarkBlue);
        padding: .5rem 1.25rem;
        cursor: pointer;
        transition: var(--trans);
        font-size: 0.9rem;
    }
    li a:hover, li a:focus {
        color: white;
        background-color: var(--softRed);
        border-radius: var(--borderRadius);
    }
    .active a {
        color: white;
        background-color: var(--softRed);
        border-radius: var(--borderRadius);
    }
    .active a:hover {
        background-color: white;
        color: var(--veryDarkBlue);
        box-shadow: 0 0 2px 2px var(--softRed);
    }
    .hamburger-btn {
        padding-right: 2rem;
        width: 55px;
        cursor: pointer;
        display: none;
    }

    @media (max-width: 775px) {
        ul {
            display: none;
        }
        .hamburger-btn {
            display: block !important;
        }
    }


</style>