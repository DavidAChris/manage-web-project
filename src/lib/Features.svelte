<script>
    import FeatureItem from "$lib/FeatureItem.svelte";
    let featureItems = [
        {header: "Track company-wide progress", content: "See how your day-to-day tasks fit into the wider vision. Go from tracking progress at the milestone level all the way down to the smallest of details. Never lose sight of the bigger picture again."},
        {header: "Advanced built-in reports", content: "Set internal delivery estimates and track progress toward company goals. Our customisable dashboard helps you build out the reports you need to keep key stakeholders informed."},
        {header: "Everything you need in one place", content: "Stop jumping form one service to another to communicate, store files, track tasks and share documents. Manage offers an all-in-one team productivity solution."}
    ]
    function handleItemNum(i) {
        return i + 1
    }
</script>

<section id="features">
    <div class="container flex flex-col px-4 mx-auto mt-10 space-y-12 md:space-y-0 md:flex-row">
        <div class="flex flex-col space-y-12 md:w-1/2">
            <h2 class="max-w-md text-4xl font-bold text-center md:text-left">
                What's different about Manage?
            </h2>
            <p class="max-w-sm text-center text-darkGrayishBlue md:text-left">
                Manage provider all the functionality your team needs, without the complexity.
                Our software is tailor-made for modern digital product teams.
            </p>
        </div>
        <div class="flex flex-col space-y-8 md:w-1/2">
            {#each featureItems as item, i (i)}
                <FeatureItem header={item.header} content={item.content} itemNum={"0" + handleItemNum(i)}/>
            {/each}
        </div>
    </div>
</section>