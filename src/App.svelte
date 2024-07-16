<script>
    import Navbar from "./Navbar.svelte";

    let navItems = [
        { text: "About", href: "/about" },
        { text: "Projects", href: "/projects" },
        { text: "Contact", href: "/contact" },
        { text: "Blog", href: "/blog" },
        { text: "Portfolio", href: "/portfolio" },
    ];

    let showNavbar = true;

    function toggleNavbar() {
        showNavbar = !showNavbar;
    }
</script>

<main>
    {#if showNavbar}
        <Navbar {navItems} />
    {/if}

    <button on:click={toggleNavbar}>
        {showNavbar ? "Hide Navbar" : "Show Navbar"}
    </button>
</main>
