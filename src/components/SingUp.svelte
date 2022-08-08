<script>
import {fade} from 'svelte/transition';

let email = "";
let open = false;
let active;
let errorText = "";

function validateEmail ()
{
  open = !open;
  let regexEmail = /^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w{2,3})+$/;
  if (email.match(regexEmail)) {
    errorText = "Thank you for subscription";
    active = "green";
  } else {
    errorText = "Whoops, make sure it's an email";
    active = "";
  }
  setInterval(() => {
    open = false;
  }, 3000);
  email = "";
}
</script>

<section>
    <h4>35.000 + ALREADY JOINED</h4>
    <h2>Stay up-to-date with what we're doing</h2>
    <form on:submit|preventDefault={validateEmail}>
        <div class="input-group">
            <input  
            bind:value={email}
            type="text" name="email" id="email" 
            placeholder="Enter your email address">
            {#if open}
                <small class:green="{active === "green" ? "green" : ''}" 
                transition:fade class="error-msg">{errorText}</small>
            {/if}
        </div>
        <button type="submit" class="btn">Contact Us</button>
    </form>
</section>

<style>
    section {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 1rem;
        padding: 4rem 1rem;
        background-color: var(--softBlue);
        margin-top: 4rem;
    }

    h2,h4 {
        color: #fff;
        text-align: center;
    }
    
    h4 {
        font-weight: normal;
    }

    button {
        background-color: var(--softRed);
    }

    button:hover {
        background: #fff;
        color: var(--softRed);
        box-shadow: 0 0 2px 2px var(--softRed);
    }

    form {
        padding-top: 1rem;
        display: flex;
        gap: 0.5rem;
        align-items: flex-start;
    }

    .input-group {
        display: flex;
        flex-direction: column;
    }

    input {
        padding: 0.8rem 1rem;
        width: 300px;
        border-radius: var(--borderRadius);
        border: none;
        outline: none;
        font-size: 1rem;
        font-weight: 500;
        color: var(--grayishBlue);
    }

    input::placeholder {
        font-size: 1rem;
        font-weight: 500;
        color: var(--grayishBlue);
    }

    .error-msg {
        text-align: center;
        width: 100%;
        background-color: var(--softRed);
        color: #fff;
        border-bottom-left-radius: var(--borderRadius);
        border-bottom-right-radius: var(--borderRadius);
        padding: 0.5rem 0;
        margin-bottom: 0.25rem;
    }

    .green {
        background-color: rgb(0, 255, 0) !important;
    }

@media(max-width:600px) {
    input {
        width: inherit;
        padding: 0.8rem 1rem;
    }
    section {
        margin-top: 2rem;
    }
}

@media(max-width:500px) {
    h2 {
        font-size: 1.75rem;
    }
    h4, button, input, input::placeholder {
        font-size: 0.9rem;
    }
    form {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 0.5rem;
        width: 100%;
    }

    input {
        width: 250px;
    }
}

@media(max-width:350px) {
    input {
        width: 100%;
    }
}

</style>