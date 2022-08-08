<script>
</script>

<main>
    <section class="column-1">
        <h1>A Simple Bookmark Manager</h1>
        <p>A clean and simple interface to organize your favourite websites. Open a new browser tan and see your sites load instantly. Try it for free.</p>
        <div class="btn-group">
            <button class="btn active">Get it on Chrome</button>
            <button class="btn inactive">Get it on Firefox</button>
        </div>
    </section>
    <section class="column-2">
        <!-- svelte-ignore a11y-img-redundant-alt -->
        <img src="../images/illustration-hero.svg" alt="hero-image">
    </section>
</main>

<style>

main {
    display: grid;
    grid-template-columns: 1.5fr 2fr;
    align-items: center;
    gap: 1rem;
    padding: 2.5rem;
}

.column-1 {
    display: flex;
    flex-direction: column;
    gap: 1rem;
}

h1 {
    font-size: 2.25rem;
}

.inactive {
    box-shadow: 0 0 2px 2px var(--lightGrayishBlue);
    background: #fff;
    color: var(--veryDarkBlue);
}

.inactive:hover, .inactive:focus {
    background: var(--softBlue);
    color: #fff;
    box-shadow: none;
}

.active {
    margin-right: 0.5rem;
}

.column-2 {
    position: relative;
}

.column-2::before {
    content: "";
    position: absolute;
    height: 80%;
    width: 78.8%;
    z-index: -1;
    top: 20%;
    left: 25%;
    border-bottom-left-radius: 30%;
    background-color: var(--softBlue);
}

.column-2 img {
    width: 100%;
}

@media (max-width: 920px) {
    main {
        display: flex;
        flex-direction: column;
        padding: 2.5rem 1rem;
        gap: 2rem;
    }

    p {
        padding: 0 1rem;
    }

    .column-1 {
        align-items: center;
        text-align: center;
    }
}

@media (max-width: 500px) { 
    h1 {
        font-size: 2rem;
    }

    p {
        padding: 0;
    }

    p, .btn {
        font-size: 0.9rem;
    }
}



</style>