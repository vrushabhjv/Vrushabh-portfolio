<script>
    import "../app.css";
    import Header from "../components/Header.svelte";
    import Footer from "../components/Footer.svelte";

    let y;
    let innerHeight = 0;
    let innerWidth = 0;

    function goTop(){
        document.body.scrollIntoView()
    }
</script>

<div class="relative flex flex-col max-w-[1400px] mx-auto w-full text-sm 
sm:text-base min-h-screen">
<!-- So, the div is essentially a fixed position element at the bottom of 
    the viewport with conditional visibility and interactivity based on the
     value of the y variable. When y is greater than 0 (i.e., the user has scrolled down the page),
    the div becomes visible and interactive; otherwise, it's hidden and non-interactive.
     This kind of behavior is often used for elements like scroll-up buttons 
     or navigation bars that appear or disappear as the user scrolls. -->
    <div class={"fixed bottom-0 w-full duration-200 flex p-10 z-[10] " + 
    (y>0? "opacity-full pointer-events-auto":" opacity-0 pointer-events-none")
    }>
        <button on:click={goTop} class="ml-auto rounded-full bg-slate-900
        text-violet-400 px-3 sm:px-4 hover:bg-slate-800 cursor-pointer">
            <i class="fa-solid fa-arrow grid place-items-center aspect-square"/>
        </button>
    </div>
    <Header y={y} />
    <slot /> 
    <Footer />
</div>

<svelte:window bind:scrollY={y} bind:innerHeight bind:innerWidth />
  
