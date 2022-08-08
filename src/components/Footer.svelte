<script>
</script>

<footer>
    <a href="#" class="logo"><img class="logo-img" src="../images/logo-bookmark white.svg" alt="logo"></a>
    <ul class="links">
        <li><a href="#">features</a></li>
        <li><a href="#">pricing</a></li>
        <li><a href="#">contact</a></li>
    </ul>
    <ul class="social-icons">
        <a href="#">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24"><path fill="#FFF" fill-rule="evenodd" d="M22.675 0H1.325C.593 0 0 .593 0 1.325v21.351C0 23.407.593 24 1.325 24H12.82v-9.294H9.692v-3.622h3.128V8.413c0-3.1 1.893-4.788 4.659-4.788 1.325 0 2.463.099 2.795.143v3.24l-1.918.001c-1.504 0-1.795.715-1.795 1.763v2.313h3.587l-.467 3.622h-3.12V24h6.116c.73 0 1.323-.593 1.323-1.325V1.325C24 .593 23.407 0 22.675 0z"/></svg>
        </a>
        <a href="#">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="20"><path fill="#FFF" fill-rule="evenodd" d="M24 2.557a9.83 9.83 0 0 1-2.828.775A4.932 4.932 0 0 0 23.337.608a9.864 9.864 0 0 1-3.127 1.195A4.916 4.916 0 0 0 16.616.248c-3.179 0-5.515 2.966-4.797 6.045A13.978 13.978 0 0 1 1.671 1.149a4.93 4.93 0 0 0 1.523 6.574 4.903 4.903 0 0 1-2.229-.616c-.054 2.281 1.581 4.415 3.949 4.89a4.935 4.935 0 0 1-2.224.084 4.928 4.928 0 0 0 4.6 3.419A9.9 9.9 0 0 1 0 17.54a13.94 13.94 0 0 0 7.548 2.212c9.142 0 14.307-7.721 13.995-14.646A10.025 10.025 0 0 0 24 2.557z"/></svg>
        </a>
    </ul>
</footer>
<div class="signature">
    Challenge by <a href="https://www.frontendmentor.io/challenges/bookmark-landing-page-5d0b588a9edda32581d29158">Frontend Mentor.</a>  Coded by <a href="https://github.com/Blaumanis">Blaumanis</a>.
</div>

<style>
    footer {
        padding: 1rem;
        background-color: var(--veryDarkBlue);
        display: flex;
        align-items: center;
        justify-content: space-evenly;
    }

    ul {
        display: flex;
        align-items: center;
        gap: 2rem;
    }

    .logo-img{
        width: 175px;
    }

    a {
        color: white;
        text-transform: uppercase;
        transition: var(--trans);
    }

    a svg path {
        transition: var(--trans);
    }

    a:hover, a:focus {
        color: var(--softRed);
    }

    a:hover svg path, a:focus svg path {
        fill: var(--softRed)
    }

    .signature {
        text-align: center;
        padding: 0.5rem;
        font-size: .8rem;
    }

    .signature a {
        color: var(--softBlue);
        text-transform: capitalize;
    }

    @media (max-width: 720px) {
        footer {
            flex-direction: column;
            gap: 1.5rem;
        }
    }

    @media (max-width: 500px) {
        footer a {
            font-size: .9rem;
        }
    }

</style>