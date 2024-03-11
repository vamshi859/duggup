<script>
    import SectionWrapper from "./SectionWrapper.svelte";
    import Logo from "../assets/svg/logo.svg";
    import home from "../assets/svg/home.svg";
    import explore from "../assets/svg/explore.svg";
    import learn from "../assets/svg/learn.svg";
    import plusSquare from "../assets/svg/plusSquare.svg";
    import navavtr from "../assets/images/navavtr.png";
    import chevdown from "../assets/svg/chevdown.svg";
    import { openModal } from "../store";
    console.log($openModal)
</script>

<header class="flex flex-col relative z-20 mx-10 mb-[50px]">
    <div
        class="max-w-[1400px] mx-auto w-full flex items-center justify-between"
    >
        <a href="/">
            <h1 class="font-semibold flex gap-1 items-center">
                <img src={Logo} alt="logo" />
                <span class="text-[#333333]">duggup</span>
            </h1>
        </a>
        <button on:click={() => ($openModal = true)} class="hidden bars-btn grid place-items-center">
            <i class="fa-solid fa-bars"></i>
        </button>
        <nav class="navbar flex items-center gap-[40px]">
            <div class="flex gap-[40px] items-center">
                <div class="flex gap-[40px] items-center">
                    <div class="flex justify-between gap-6 items-center">
                        <button class="nav-btn flex gap-2 items-center">
                            <img src={home} alt="home" />
                            <p class="font-[400] text-[14px] leading-[20px]">
                                Home
                            </p>
                        </button>
                        <button class="nav-btn flex gap-2 items-center">
                            <img src={explore} alt="explore" />
                            <p class="font-[400] text-[14px] leading-[20px]">
                                Explore
                            </p>
                        </button>
                        <button class="nav-btn flex gap-2 items-center">
                            <img src={learn} alt="learn" />
                            <p class="font-[400] text-[14px] leading-[20px]">
                                Learn
                            </p>
                        </button>
                    </div>
                    <button class="specialBtn flex gap-3 items-center">
                        <img src={plusSquare} alt="plusSquare" />
                        <p class="font-[400] text-[14px] leading-[20px]">
                            Post
                        </p>
                    </button>
                </div>
                <div class="flex items-center gap-3 explore-tab cursor-pointer">
                    <img
                        src={navavtr}
                        class="navavtr w-[48px] h-[48px] p-1"
                        alt="navavtr"
                    />
                    <p class="font-[500] text-[20px] leading-[24px]">
                        Krishna Kiran
                    </p>
                    <img src={chevdown} alt="chevdown" />
                </div>
            </div>
        </nav>
    </div>
    <div class="horizontal-line px-2" />
</header>
