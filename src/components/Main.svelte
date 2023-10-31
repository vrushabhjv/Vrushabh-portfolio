<script>
    import Step from "../components/Step.svelte";

    let steps=[
        {name:'Store',icon:'fa-solid fa-cart-shopping'},
        // icon used are from fontsawesome.com
        {name:'ToDos',icon:'fa-solid fa-list-check'},
        {name:'poke',icon:'fa-solid fa-diagram-project'}
    ]
    let benefits=[
        {name:'a self taught developer',description:' lorem ipsum dolor sit amet consectetur adipisicing elit. '},
        {name:'a cloud enthusiast',description:'lorem ipsum dolor sit amet consectetur adipisicing elit.'},
        {name:'an excellent communicator',description:'lorem ipsum dolor sit amet consectetur adipisicing elit.'}
    ]
</script>

<main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
        <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
            <h2 class="font-semibold text-4xl sm:text-5xl lg:text-6xl">
                Hi! I'm <span class="poppins text-violet-400 hover:font-bold hover:text-violet-600">Vrushabh J V</span><br>
                <span class="poppins text-violet-400 hover:font-bold hover:text-violet-600">Cloud</span> Developer
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                My <span class="poppins text-violet-400 hover:font-semibold">favorite tech</span> includes
                AWS, Python, JavaScript, Node.js + Express.js, PostgreSQL, and MongoDB.
            </p>
            <p class="text-base sm:text-lg md:text-xl">
                I'm currently working on <span class="poppins text-violet-400">AWS</span> and <span class="poppins text-violet-400">Python</span> projects.
            </p>
            <a href="https://www.linkedin.com/in/vrushabh-j-v-91155a229" 
                target="_blank"
                class="blueShadow mx-auto lg:mx-auto text-base sm:text-lg md:text-xl
                poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white 
                text-slate-950 cursor-pointer hover:bg-violet-900 hover:text-white duration-200">
                <div class="absolute top-0 right-full w-full h-full bg-violet-900 opacity-50
                group-hover:translate-x-full z-0 duration-300">
                </div>
                <h4 class="relative z-9 font-semibold">Get in touch &rarr;</h4>

            </a>
        </div>

        <div class="relative shadow-2xl grid place-items-center">
            <img src={"images/profile.png"} alt="profile image" 
            class="object-cover z-[2] max-h-[70vh]"/>
        </div>


    </section>


    <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-lg sm:text-xl md:text-2xl">
                Some of my creative endeavors.
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Curious to <span class="poppins text-violet-400">see</span> my work?
            </h3>
        </div>
        <a href="https://www.youtube.com/"
            target="_blank" class="mx-auto px-4 py-2 rounded-md border border-solid border-white
            flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-violet-700 duration-200">
            <i class="fa-regular fa-circle-play"/>
            <p>Watch the video</p>
        </a>
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>
                    This store is a merchandizing store created with <strong class="text-violet-400">Next.js 
                    Commerce.js Stripe & Node.js + Express.js</strong> Commerce.js is a product CMS and 
                    Stripe is used for payment processing.
                </p>

            </Step>
            <Step step={steps[1]}>
                <p>
                    This store is a merchandizing store created with <strong class="text-violet-400">Next.js 
                    Commerce.js Stripe & Node.js + Express.js</strong> Commerce.js is a product CMS and 
                    Stripe is used for payment processing.
                </p>

            </Step>
            <Step step={steps[2]}>
                <p>
                    This store is a merchandizing store created with <strong class="text-violet-400">Next.js 
                    Commerce.js Stripe & Node.js + Express.js</strong> Commerce.js is a product CMS and 
                    Stripe is used for payment processing.
                </p>

            </Step>
        </div>

    </section>

    <section id="about" class="py-20 pt-10 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative">
        <div class="flex flex-col gap-2 text-center relative before:absolute before:top-0 
        before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 
        after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4">
            <h6 class="text-lg sm:text-xl md:text-2xl">Want to know more?</h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                A bit <span class="poppins text-violet-400">about</span> me.
            </h3>
        </div>

        <p class="mx-auto poppins font-semibold text-xl sm:text-2xl md:text-3xl">I am . . .</p>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each benefits as benifit, index}
                <div class="flex gap-6 sm:gap-8">
                    <p class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500
                    font-semibold">
                        0{index+1}.
                    </p>
                    <div class="flex flex-col gap-6 sm:gap-8">
                        <h3 class="text-3xl sm:text-4xl md:text-5xl">
                            {benifit.name}
                        </h3>
                        <p>{benifit.description}</p>
                    </div>
                </div>
            {/each}
        </div>
        <h5 class="text-2xl sm:text-3xl font-semibold text-center poppins">
            The <span class="poppins text-violet-400">Complete</span> Package
        </h5>
        <div class="flex flex-col overflow-x-scroll gap-10 max-w-[800px] mx-auto w-full">

        </div>
    </section>
</main>