<script>
    import SimpleCard from "$lib/components/SimpleCard.svelte";
    
    //Dummy Data 4 Mockups
    const projects = [
        "Sample1",
        "Sample2",
        "Sample3",
        "Sample4"
]
</script>

<!-- TODO: ARCHIVE LAYOUT -->
<!-- Sample of the basic idea for the archive view -->
<div class="flexbox space-y-2">
    {#each projects as p}
         <!-- content here -->
        <SimpleCard>
            {p}
        </SimpleCard>

    {/each}
</div>