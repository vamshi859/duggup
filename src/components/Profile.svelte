<script>
    import navavtr from "../assets/images/navavtr.png";
    import SectionWrapper from "./SectionWrapper.svelte";
    import logo from "../assets/images/logo.png";
    import redirect from "../assets/svg/redirect.svg";
    import ellipsis from "../assets/svg/ellipsis.svg";
    let follow = false;
</script>

<SectionWrapper>
    <div class="flex gap-[30px]">
        <div class="flex flex-col justify-center gap-2 items-center">
            <img src={navavtr} class="profile-avtr w-[120px] h-[120px]" alt="navavtr" />
            <p class="profile-name font-[700] text-[24px] leading-[28px] text-center w-[156px]">Krishna Kiran</p>
        </div>
        <div class="flex flex-col gap-[20px] py-3">
            <div class="grid justify-between grid-cols-3">
                <p class="profile-content col-span-2 font-[400] text-[14px] leading-[24px]">Co-Founder and CEO at Duggup - Social network for people in tech. Ex-Amazon Head of Engineering. I write hot-takes on building a business, shipping delightful products and accelerating product and career growth.</p>
                <div class="flex flex-col col-span-1 items-end gap-[8px] pr-[96px]">
                    <img src={logo} class="w-[36px] h-[36px]" alt="logo"/>
                    <div class="flex flex-col gap-[4px] items-end">
                        <p class="duggup font-[700] text-[16px] leading-[19.36px]">Duggup</p>
                        <p class="ceo text-right font-[400] text-[12px] leading-[14.52px]">Co-Founder and CEO</p>
                    </div>
                </div>
            </div>
            <div class="flex justify-between items-center">
                <button on:click={() => (follow = !follow)} class={`followBtn ${follow ? 'drop-shadow' : ''} font-[400] text-[14px] leading-[20px]`}>
                    {follow ? 'Followed' : 'Follow'}
                </button>
                <div class="flex gap-[16px] items-center pr-[96px]">
                    <button class="flex gap-[4px] items-center">
                        <p class="font-[400] text-[14px] leading-[20px]">My website</p>
                        <img src={redirect} alt="redirect" />
                    </button>
                    <img src={ellipsis} alt="ellipsis" />
                </div>
            </div>
        </div>
    </div>
</SectionWrapper>