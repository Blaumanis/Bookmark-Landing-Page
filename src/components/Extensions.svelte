<script>

</script>

<section>
    <div class="section-header">
        <h2>Dowload the extension</h2>
        <p>We've got more browsers in the pipeline. 
        Please do let us know if you've got a favourite you'd like us to prioritize.</p>
    </div>
    <div class="article-wrapper">
        <article class="chrome">
            <img src="../images/logo-chrome.svg" alt="chrome-logo">
            <h4>Add to Chrome</h4>
            <small>Minimum version 62</small>
            <img src="../images/bg-dots.svg" alt="dots" class="dot-separator">
            <button class="btn">Add & install Extension</button>
        </article>
        <article class="firefox">
            <img src="../images/logo-firefox.svg" alt="firefox-logo">
            <h4>Add to Firefox</h4>
            <small>Minimum version 55</small>
            <img src="../images/bg-dots.svg" alt="dots" class="dot-separator">
            <button class="btn">Add & install Extension</button>
        </article>
        <article class="opera">
            <img src="../images/logo-opera.svg" alt="opera-logo">
            <h4>Add to Opera</h4>
            <small>Minimum version 46</small>
            <img src="../images/bg-dots.svg" alt="dots" class="dot-separator">
            <button class="btn">Add & install Extension</button>
        </article>
    </div>
</section>

<style>

section {
    display: flex;
    align-items: center;
    flex-direction: column;
    gap: 4rem;
    padding: 6rem 1rem 4rem;
    text-align: center;
}

h2 {
    padding-bottom: 1rem;
}

p {
    width: 600px;
}

.article-wrapper {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 1rem;
}

article {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 270px;
    padding: 2rem 1rem;
    box-shadow: 0 0 2px 2px var(--lightGrayishBlue);
    border-radius: var(--borderRadius);
}

.chrome {
    margin-bottom: 4rem;
}

.firefox {
    margin-bottom: 3rem;
}

.opera {
    margin-bottom: 2rem;
}

article img {
    padding-bottom: 2rem;
}

article h4 {
    font-size: 1.5rem;
}

article small {
    color: var(--grayishBlue);
    font-size: 1rem;
}

.dot-separator {
    padding: 2rem 0;
    width: 270px;
}

@media (max-width: 920px) {
    .article-wrapper {
        flex-wrap: wrap;
    }

    article {
        margin: 0 !important;
    }
}

@media (max-width: 600px) {
    section {
        gap: 2rem;
    }
    article, p, .dot-separator {
        width: 100%;
    }
}

@media (max-width: 500px) {
    h2 {
        font-size: 1.75rem;
    }
    article h4 {
        font-size: 1.25rem;
    }
    p, article small, .btn {
        font-size: 0.9rem;
    }
}

</style>