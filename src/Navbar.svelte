<main>
    <h3>About</h3>
    <h3>Projects</h3>
    <h3>Contact</h3>
    <h3>Blog</h3>
    <h3>Portfolio</h3>
</main>

<style>
    h3 {
        font-family: "SF Mono", monospace;
        position: relative;
        cursor: pointer;

        transition: letter-spacing 0.25s ease-out;
    }

    main {
        display: flex;
        justify-content: space-between;
        padding: 0 2rem;
    }

    h3:hover {
        letter-spacing: 1px;
    }

    h3::after {
        content: '';
        position: absolute;
        width: 0;
        height: 2px;
        bottom: -5px;
        left: 0;
        background-color: red;
        transition: width 0.25s ease-out;
    }

    h3:hover::after {
        width: 100%;
    }

    @keyframes underline-hover {
        0%, 100% {
            width: 0;
        }
        50% {
            width: 100%;
        }
    }
</style>