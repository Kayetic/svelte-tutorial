<script>
    export let navItems = [
        { text: "About", href: "/about" },
        { text: "Projects", href: "/projects" },
        { text: "Contact", href: "/contact" },
        { text: "Blog", href: "/blog" },
        { text: "Portfolio", href: "/portfolio" },
    ];
</script>

<nav>
    {#each navItems as item}
        <a href={item.href}>{item.text}</a>
    {/each}
</nav>

<style>
    nav {
        display: flex;
        justify-content: space-between;
        padding: 0 2rem;
        margin: 1.5rem 0;
    }

    a {
        font-family: "SF Mono", monospace;
        position: relative;
        cursor: pointer;
        text-decoration: none;
        color: inherit;
        transition: letter-spacing 0.25s ease-out;
    }

    a:hover {
        letter-spacing: 1px;
    }

    a::after {
        content: "";
        position: absolute;
        width: 0;
        height: 2px;
        bottom: -5px;
        left: 0;
        background-color: red;
        transition: width 0.25s ease-out;
    }

    a:hover::after {
        width: 100%;
    }

    @keyframes underline-hover {
        0%,
        100% {
            width: 0;
        }
        50% {
            width: 100%;
        }
    }
</style>
