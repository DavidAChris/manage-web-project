<script>
    import ImgContainer from "$lib/ImgContainer.svelte";

    let socialLinks = [
        "https://raw.githubusercontent.com/bradtraversy/tailwind-landing-page/main/img/icon-facebook.svg",
        "https://raw.githubusercontent.com/bradtraversy/tailwind-landing-page/main/img/icon-youtube.svg",
        "https://raw.githubusercontent.com/bradtraversy/tailwind-landing-page/main/img/icon-twitter.svg",
        "https://raw.githubusercontent.com/bradtraversy/tailwind-landing-page/main/img/icon-pinterest.svg",
        "https://raw.githubusercontent.com/bradtraversy/tailwind-landing-page/main/img/icon-instagram.svg",

    ]
    let leftContainerList = ["Home", "Pricing", "Products", "About"]
    let rightContainerList = ["Careers", "Community", "Privacy Policy"]
</script>


<footer class="bg-veryDarkBlue">
    <!--    FLex Container-->
    <div class="container flex flex-col-reverse justify-between px-6 py-10 mx-auto space-y-8 md:flex-row md:space-y-0">
        <!--        Logo and Social links container-->
        <div class="flex flex-col-reverse items-center justify-between space-y-12 md:flex-col md:space-y-0 md:items-start">
            <div class="mx-auto my-6 text-center text-white md:hidden">Copyright &copy; 2022, All Rights Reserved</div>
            <!--            Logo-->
            <ImgContainer
                    src="https://raw.githubusercontent.com/bradtraversy/tailwind-landing-page/main/img/logo-white.svg"
                    imgClass="h-8"/>
            <!--            Social Links Container-->
            <div class="flex justify-center space-x-4">
                {#each socialLinks as link, i (i)}
                    <a href="#">
                        <img src={link} class="h-8">
                    </a>
                {/each}
            </div>
        </div>
        <!--        List Container-->
        <div class="flex justify-around space-x-32 px-4">
            <div class="flex flex-col space-y-3 text-white">
                {#each leftContainerList as item, i (i)}
                    <a href="#" class="hover:text-brightRed">{item}</a>
                {/each}
            </div>
            <div class="flex flex-col space-y-3 text-white">
                {#each rightContainerList as item, i (i)}
                    <a href="#" class="hover:text-brightRed">{item}</a>
                {/each}
            </div>
        </div>
        <!--        Input Container-->
        <div class="flex flex-col justify-between">
            <form>
                <div class="flex space-x-3">
                    <input type="text" class="flex-1 px-4 rounded-full focus:outline-none"
                           placeholder="Update in your inbox"/>
                    <button class="px-6 py-2 text-white rounded-full bg-brightRed hover:bg-brightRedLight focus:outline-none">
                        Go
                    </button>
                </div>
            </form>
            <div class="hidden text-white md:block">
                Copyright &copy; 2022, All Rights Reserved
            </div>
        </div>
    </div>
</footer>