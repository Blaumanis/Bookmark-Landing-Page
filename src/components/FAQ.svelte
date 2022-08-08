<script>
    import {slide} from 'svelte/transition';
    let current;
    let open = false;
    function openAnswer(e) {
        open = !open
        if(e.target.classList.contains('first')) {
            current = "answerA"
        }
        else if(e.target.classList.contains("second")) {
            current = "answerB"
        }
        else if(e.target.classList.contains("third")) {
            current = "answerC"
        }
        else {
            current = "answerD"
    }
}

</script>

<section>
    <div class="section-header">
        <h2>Frequently Asked Questions</h2>
        <p>Here are some of our FAQs. if you have any other questions you'd like answered please feel free to email us.</p>
    </div>
    <div class="faqs">
       <div on:click={openAnswer} class="faq">
            <h4 class="first">What is Bookmark? <img src="../images/icon-arrow.svg" alt="icon-arrow"></h4>
            {#if open}
                <p transition:slide class:active-answer="{current === "answerA"}" class="answer answerA">Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptatem quo ab nisi doloremque pariatur sint culpa quod, voluptate rerum quibusdam reiciendis, cumque expedita totam animi asperiores illo voluptas? Perferendis, perspiciatis!</p>
            {/if}
       </div>
       <div on:click={openAnswer} class="faq">
            <h4 class="second">How can i request a new browser? <img src="../images/icon-arrow.svg" alt="icon-arrow"></h4>
            {#if open}
                <p transition:slide class:active-answer="{current === "answerB"}" class="answer answerB">Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptatem quo ab nisi doloremque pariatur sint culpa quod, voluptate rerum quibusdam reiciendis, cumque expedita totam animi asperiores illo voluptas? Perferendis, perspiciatis!</p>
            {/if}
        </div> 
        <div on:click={openAnswer} class="faq">
            <h4 class="third">Is there a mobile app? <img src="../images/icon-arrow.svg" alt="icon-arrow"></h4>
            {#if open}
                <p transition:slide class:active-answer="{current === "answerC"}" class="answer answerC">Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptatem quo ab nisi doloremque pariatur sint culpa quod, voluptate rerum quibusdam reiciendis, cumque expedita totam animi asperiores illo voluptas? Perferendis, perspiciatis!</p>
            {/if}
        </div> 
        <div on:click={openAnswer} class="faq">
            <h4 class="fourth">What about other Chromium browsers? <img src="../images/icon-arrow.svg" alt="icon-arrow"></h4>
            {#if open}
                <p transition:slide class:active-answer="{current === "answerD"}" class="answer answerD">Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptatem quo ab nisi doloremque pariatur sint culpa quod, voluptate rerum quibusdam reiciendis, cumque expedita totam animi asperiores illo voluptas? Perferendis, perspiciatis!</p>
            {/if}
        </div> 
    </div>
    <button class="btn">More info</button>
</section>

<style>

section {
    display: flex;
    align-items: center;
    flex-direction: column;
    padding: 2rem 1rem;
    text-align: center;
}

.section-header {
    padding-bottom: 4rem;
}

h2 {
    padding-bottom: 1rem;
}

.section-header p {
    width: 600px;
}

.faqs {
    display: flex;
    align-items: flex-start;
    flex-direction: column;
    width: 600px;
    padding-bottom: 3rem;
}

.faq {
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-direction: column;
    width: 100%;
    cursor: pointer;
}

.faq h4 {
    width: 100%;
    text-align: left;
    padding: 1rem 0;
    padding-left: .5rem;
    border-bottom: 1px solid var(--lightGrayishBlue);
    transition: var(--trans);
}

.faq h4:hover {
    background-color: var(--lightGrayishBlue);
}

.faq img {
    padding-right: .5rem;
    float: right;
    pointer-events: none;
}

.answer {
    text-align: left;
    padding-left: 0.5rem;
    padding-top: 2rem;
}

.answer {
    display: none;
}

@media(max-width:650px) {
    .section-header p {
        width: 100%;
    }

    .section-header {
        padding-bottom: 2rem;
    }

    .faqs {
        width: 100%;
        align-items: center;
        padding-bottom: 2rem;
    }
}

@media(max-width:500px) {
    h2 {
        font-size: 1.75rem;
    }
    h4, p, button {
        font-size: 0.9rem;
    }
    .faq {
        width: 300px;
    }
}


</style>