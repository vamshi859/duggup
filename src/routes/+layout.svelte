<script>
    import "../app.css";
    import Logo from "../assets/svg/logo.svg";
    import {openModal} from "../store";

    function reroute(href) {
        $openModal = false;
        window.location.href = href;
    }

</script>

{#if $openModal}
    <div
        class="modal-bar hidden fixed top-0 left-0 w-screen h-screen border-b bg-white z-50 flex flex-col z-20"
    >
        <div class="flex items-center justify-between gap-4 mx-10">
            <a href="/">
                <h1 class="font-semibold flex gap-1 items-center">
                    <img src={Logo} alt="logo" />
                    <span class="text-[#333333]">duggup</span>
                </h1>
            </a>
            <button
                on:click={() => ($openModal = false)}
                class="outline-none border-none cross-btn"
            >
                <i class="fa-solid fa-xmark text-2xl"></i>
            </button>
        </div>
        <div class="horizontal-line px-2" />
        <div class="flex flex-col gap-4 flex-1 mt-5">
            <button
                on:click={() => reroute("#product")}
                class="border-none outline-none p-2 group duration-200 cursor-pointer text-left"
            >
                <p
                    class="duration-200 group-hover:pl-2 poppins text-3xl font-semibold"
                >
                    Home <i class="fa-solid fa-chevron-right text-xl pl-4" />
                </p>
            </button>
            <button
                on:click={() => reroute("#reviews")}
                class="border-none outline-none p-2 group duration-200 cursor-pointer text-left"
            >
                <p
                    class="duration-200 group-hover:pl-2 poppins text-3xl font-semibold"
                >
                    Explore <i class="fa-solid fa-chevron-right text-xl pl-4" />
                </p>
            </button>
            <button
                on:click={() => reroute("#faqs")}
                class="border-none outline-none p-2 group duration-200 cursor-pointer text-left"
            >
                <p
                    class="duration-200 group-hover:pl-2 poppins text-3xl font-semibold"
                >
                    Learn <i class="fa-solid fa-chevron-right text-xl pl-4" />
                </p>
            </button>
        </div>
    </div>
{/if}
<slot />

<!-- header
hero
product description
user reviews
faq
conversion
footer -->
