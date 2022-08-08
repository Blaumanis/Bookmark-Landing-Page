<script>
    import { fade } from 'svelte/transition';
    let current = "Simple Bookmarking";
    let activeArticle = "bookmark";

    function showContent(e){
        if(e.target.classList.contains("simple")){
            current = "Simple Bookmarking";
            activeArticle = "bookmark";
        } 
        else if(e.target.classList.contains("easy")) {
            current = "Easy Sharing";
            activeArticle = "easy"
        }
        else {
            current = "Speedy Searching";
            activeArticle = "speedy"
        }
    }
</script>

<section class="features-container">
    <article class="features-header">
        <h2>Features</h2>
        <p>Our aim is to make it quick and easy for you to access your favourite websites. 
            Your bookmarks sync between your devices so you can access them on the go</p>
        <div class="btn-group">
            <button class:active="{current === 'Simple Bookmarking'}" class="btn btn-gray simple" on:click={showContent}>Simple Bookmarking</button>
            <button class:active="{current === 'Easy Sharing'}" class="btn btn-gray easy" on:click={showContent}>Easy Sharing</button>
            <button class:active="{current === 'Speedy Searching'}" class="btn btn-gray speedy" on:click={showContent}>Speedy Searching</button>
        </div>
    </article>

    {#if activeArticle === "bookmark"}
        <article class="section-content" transition:fade>
            <div class="column-1">
                <img src="../images/illustration-features-tab-1.svg" alt="first-tab">
            </div>
            <div class="column-2">
                <h3>Bookmark in one click</h3>
                <p>Organize your bookmarks however you like. Our simple drag-and-drop interface gives you complete control over how you manage your favourite sites</p>
                <button class="btn">More info</button>
            </div>
        </article>
    {:else if activeArticle === "easy"}
        <article class="section-content" transition:fade>
            <div class="column-1">
                <img src="../images/illustration-features-tab-3.svg" alt="third-tab">
            </div>
            <div class="column-2">
                <h3>Easy Sharing</h3>
                <p>Easily share your bookmarks and collections with other. Create a shareble link that you can send at the click of a button</p>
                <button class="btn">More info</button>
            </div>
        </article>
    {:else}
        <article class="section-content" transition:fade>
            <div class="column-1">
                <img src="../images/illustration-features-tab-2.svg" alt="second-tab">
            </div>
            <div class="column-2">
                <h3>Speedy Searching</h3>
                <p>Our powerful search feature will help you find saved sites in no time t all. No need to trawl through all of your bookmarks</p>
                <button class="btn">More info</button>
            </div>
        </article>
    {/if}

</section>

<style>

.features-container {
    padding: 4rem 0;
}

.features-header {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 1rem;
    text-align: center;
    padding: 0 1rem;
}

.features-header p {
    width: 600px;
}

.btn-group {
    width: 546px;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 1rem;
    padding-top: 1rem;
    border-bottom: 1px solid var(--grayishBlue);
}

.btn-gray {
    color: var(--grayishBlue);
    background-color: #fff;
    border-bottom: 4px solid #fff;
    border-radius: 0;
}

.btn-gray:hover {
    box-shadow: 0 0 2px 2px var(--lightGrayishBlue);
    border-bottom: 4px solid var(--softRed);
    color: var(--veryDarkBlue);
}

.btn-gray.active {
    border-bottom: 4px solid var(--softRed);
    color: var(--veryDarkBlue);
    box-shadow: 0 0 2px 2px var(--lightGrayishBlue);
}

.section-content {
    display: grid;
    grid-template-columns: 1.5fr 1fr;
    justify-items: center;
    align-items: center;
    padding-top: 4rem;
}

.column-1 {
    position: relative;
}

.column-1::after {
    content: "";
    position: absolute;
    height: 100%;
    width: 200%;
    z-index: -1;
    top: 25%;
    left: -120%;
    border-bottom-right-radius: 30%;
    background-color: var(--softBlue);
}

.column-1 img {
    width: 450px;
}

.column-2 {
    padding: 0 1rem;
}

.column-2 h3 {
    font-size: 1.75rem;
}

.column-2 p {
    padding: 1rem 0;
}

@media (max-width: 920px) {
    .features-container p {
        width: 90%;
    }
    .section-content {
        display: flex;
        flex-direction: column-reverse;
        text-align: center;
        gap: 2rem;
    }

    .column-1 img {
        width: 100%;
        padding: 0 1rem;
    }
}

@media (max-width: 600px) {
    .features-container {
        padding-top: 2rem;
    }
    .features-container p {
        width: 100%;
    }
    .section-content {
        padding-top: 2rem;
    }
    .btn-group {
        flex-direction: column;
        width: 100%;
        border: none;
    }
}

@media (max-width: 500px) {
    .features-header h2 {
        font-size: 1.75rem;
    }
    .column-2 h3 {
        font-size: 1.5rem;
    }
    p, button {
        font-size: 0.9rem;
    }
}


</style>