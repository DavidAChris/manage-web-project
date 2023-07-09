<script>
    import "../app.css"
    import GetButton from "$lib/GetButton.svelte";
    import ImgContainer from "$lib/ImgContainer.svelte";
    import Footer from "$lib/Footer.svelte";

    let menuItems = [
        {href: "#", content: "Pricing"},
        {href: "#", content: "Product"},
        {href: "#", content: "About Us"},
        {href: "#", content: "Careers"},
        {href: "#", content: "Community"}
    ]
    let logoContainer = {
        containClass: "pt-2",
        src: "https://raw.githubusercontent.com/bradtraversy/tailwind-landing-page/main/img/logo.svg",
        alt: "Company Logo"
    }

    function handleHamburger() {
        const btn = document.getElementById('menu-btn')
        const nav = document.getElementById('menu')

        btn.classList.toggle('open');
        nav.classList.toggle('flex');
        nav.classList.toggle('hidden');
    }
</script>

<nav class="relative container mx-auto p-6">

    <div class="flex items-center justify-between">
        <ImgContainer {...logoContainer} />
        <!--        Menu Items-->
        <div class="hidden md:flex space-x-6">
            {#each menuItems as item (item.content)}
                <a href={item.href} class="hover:text-darkGrayishBlue">{item.content}</a>
            {/each}
        </div>

        <!--        Button-->
        <GetButton content="Get Started"/>
        <!--        Hamburger-->
        <button class="block hamburger md:hidden focus:outline-none" id="menu-btn" on:click={handleHamburger}>
            <span class="hamburger-top"></span>
            <span class="hamburger-middle"></span>
            <span class="hamburger-bottom"></span>
        </button>
    </div>
    <div class="md:hidden">
        <div class="absolute flex-col items-center hidden self-end py-8 mt-10 space-y-6 font-bold bg-white sm:w-auto sm:self-center left-6 right-6 drop-shadow-md"
             id="menu">
            {#each menuItems as item (item.content)}
                <a href={item.href}>{item.content}</a>
            {/each}
        </div>
    </div>

</nav>

<slot/>

<Footer />

