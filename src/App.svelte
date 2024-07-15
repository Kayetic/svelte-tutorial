<script>
    import Navbar from './Navbar.svelte';

    let navItems = [
        { text: 'About', href: '/about' },
        { text: 'Projects', href: '/projects' },
        { text: 'Contact', href: '/contact' },
        { text: 'Blog', href: '/blog' },
        { text: 'Portfolio', href: '/portfolio' }
    ];
</script>

<main>
    <Navbar {navItems} />
</main>