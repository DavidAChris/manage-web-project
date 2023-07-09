<script>
    import TestimonialItem from "$lib/TestimonialItem.svelte";
    import GetButton from "$lib/GetButton.svelte";

    let testimonialInfo = [
        {
            personName: "Anisha Li",
            quote: "Manage has supercharged out team's workflow. The ability to maintain visibility on larger milestones at all times keeps everyone motivated.",
            personImg: "https://raw.githubusercontent.com/bradtraversy/tailwind-landing-page/main/img/avatar-anisha.png"
        }, {
            personName: "Ali Bravo",
            quote: "We have been able to cancel so many other subscriptions since using Manage. There is no more cross-channel confusion and everyone is much more focused.",
            personImg: "https://raw.githubusercontent.com/bradtraversy/tailwind-landing-page/main/img/avatar-ali.png"
        }, {
            personName: "Richard Watts",
            quote: "Manage has supercharged out team's workflow. The ability to maintain visibility on larger milestones at all times keeps everyone motivated.",
            personImg: "https://raw.githubusercontent.com/bradtraversy/tailwind-landing-page/main/img/avatar-richard.png"
        }
    ]
</script>

<section id="testimonials">
    <div class="max-w-6xl px-5 mt-32 mx-auto text-center">
        <h2 class="text-4xl font-bold text-center">What's Different About Manage?</h2>
        <div class="flex flex-col mt-24 md:flex-row md:space-x-6">
            {#each testimonialInfo as info, i (i)}
                {#if i < 1}
                    <TestimonialItem {...info} first={true}/>
                {:else }
                    <TestimonialItem {...info}/>
                {/if}
            {/each}
        </div>
        <div class="my-16">
            <GetButton content="Get Started"
                       classes="p-3 px-6 text-white bg-brightRed rounded-full baseline hover:bg-brightRedLight"/>
        </div>
    </div>
</section>