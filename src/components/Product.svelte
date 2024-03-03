<script lang="ts">
  import SectionWrapper from "./SectionWrapper.svelte";
  import ProductCard from "./ProductCard.svelte";

  interface ProductFeature {
        index: number;
        featureList: string[];
        description: string;
        imgUrl: string;
    }

  const productFeatures: ProductFeature[] = [
    {
        index: 0,
        featureList: [
            'Daily streak counter',
            'Weights and reps tracker',
            'Community challenges',
            'Exciting  and varied workouts',
        ],
        description: "With Zenith Studio, you'll have everything you need to train safely and effectively.",
        imgUrl: "assets/selection.png",
    },
    {
        index:1,
        featureList: [
            'Select your preferences',
            'Personalize your workouts',
            'Customize your training',
            'Full-body progress on every muscle group',
        ],
        description: "Gamify your regimen through streaks and quests, then plan ahead with in-depth tracking, analytics, and feedback from your coach.",
        imgUrl: "assets/training.png",
    },
    {
        index:2,
        featureList: [
            'Elimate guesswork',
            'Save time',
            'Achieve consistent results',
            'Increase overall health and strength',
        ],
        description: "By combining powerful AI with our expert coaches, you can be confident that every workout and meal is perfectly tailored to your unique needs.",
        imgUrl: "assets/goal.png",
    },

  ]

</script>
<SectionWrapper id="product">
    <div class="flex flex-col gap-10 sm:gap-14 md:gap-24 flex-1 items-center justify-center pb-10 md:pb-14">
        <div class="flex flex-col gap-2">
            <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
                Supercharge your <span class="text-indigo-400">fitness journey</span>
                today.
            </p>
            <h3 class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center">
                Features for everyone.
            </h3>
        </div>
            {#each productFeatures as productFeature}
                <ProductCard {productFeature}>
                    {#if productFeature.index===0}
                        The tools you need to train like a <span class="text-indigo-400 font-medium">
                            master
                        </span>
                    {:else if productFeature.index===1}
                        Lay the foundations for <span class="text-indigo-400 font-medium">
                            routine
                        </span>
                        and consistency
                    {:else}
                        Workouts specific to your <span class="text-indigo-400 text-medium">
                            goals
                        </span> and <span class="text-indigo-400 text-medium">
                            skill level
                        </span>
                    {/if}

                </ProductCard>
            {/each}
    </div>
</SectionWrapper>