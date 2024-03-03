<script>
    import Header from "./Header.svelte";
    import CTA from "./CTA.svelte";
    import SectionWrapper from "./SectionWrapper.svelte";
  import Stars from "./Stars.svelte";

</script>
<SectionWrapper id="hero">
    <Header />
    <div class="flex flex-col gap-10 flex-1 items-center justify-center pb-10 md:pb-14">
        <h2 class="font-semibold text-5xl sm:text-6xl md:text-7xl lg:text-8xl max-w-[1200px] mx-auto w-full text-center">
            <span class="text-indigo-400">Massive</span> gains have never been so <span class="text-indigo-400">simple</span>.
        </h2>
        <p class="text-xl sm:text-2xl md:text-3xl text-center max-w-[1000px] mx-auto w-full">
            Science-backed diet and workout plans. Personalized 1:1 coaching. Gains beyond your wildest dreams.
        </p>
        <CTA />
        <Stars />
    </div>
</SectionWrapper>