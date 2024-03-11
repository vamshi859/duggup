<script lang="ts">
    import SectionWrapper from './SectionWrapper.svelte';
    import image1 from "../assets/images/image1.png";
    import image2 from "../assets/images/image2.png";
    import image3 from "../assets/images/image3.png";
    import image4 from "../assets/images/image4.png";
    import arrowUp from "../assets/svg/chevup.svg";
    import logo from "../assets/images/logo.png";
    import logo2 from "../assets/images/logo2.png";

    // let date: string;
    // let title: string;
    // let description: string;
  
    const timelineItems = [
      {
        date: 'Jan 2023',
        works: [
          {
            image: image1,
            content: 'No amount of technology can convert a bad story into a good story.'
          },
          {
            image: image2,
            content: "Most people don't have original ideas. Here is how Sam Altman pushes himself to have unpopular ideas."
          }
        ],
        company: {
          logo: logo,
          title: 'Duggup',
          location: 'San Francisco Bay Area',
          joiningDate: 'Nov 2023',
          position: 'Co-Founder and CEO',
          duration: 'Full-time · Remote'
        }
      },
      {
        date: 'Dec 2023',
        works: [
          {
            image: image3,
            content: "Startup Lesson I am reflecting. Don't build for the 'average person'."
          },
          {
            image: image4,
            content: "Your biggest regrets at 80 will be acts of omission."
          }
        ],
        company: {
          logo: logo2,
          title: 'BetterUp',
          location: 'San Francisco Bay Area',
          joiningDate: 'Sep 2022',
          position: 'VP Engineering',
          duration: 'Full-time'
        }
      }
    ];
  </script>
  
  <SectionWrapper>
    <div class="timeline after:w-[2px] after:bottom-0">
      {#each timelineItems as timeline}
      <div class="container">
        <div class="date">{timeline.date}</div>
        <div class="content grid grid-cols-3 gap-[36px]">
          {#each timeline.works as work}
          <div class="card">
            <img src={work.image} alt={work.image} class="h-[136px]" />
            <div class="p-[24px]">
              <p class="card-content font-[400] text-[14px] leading-[21px]">{work.content}</p>
            </div>
          </div>
          {/each}
        </div>
        <div class="position-details">
          <div class="arrowUp">
            <img src={arrowUp} alt="arrowUp" class="" />
          </div>
          <div class="left-content flex flex-col col-span-1 items-end gap-[8px]">
              <img src={timeline.company.logo} class="w-[36px] h-[36px]" alt={timeline.company.logo}/>
              <div class="flex flex-col gap-[4px] items-end">
                  <p class="duggup font-[700] text-[16px] leading-[19.36px]">{timeline.company.title}</p>
                  <p class="ceo text-right font-[400] text-[12px] leading-[14.52px]">{timeline.company.location}</p>
                  <p class="ceo text-right font-[400] text-[12px] leading-[14.52px]">Joined<br />{timeline.company.joiningDate}</p>
              </div>
          </div>
          <div class="right-content flex flex-col justify-center gap-[4px]">
            <p class="title font-[700] text-[20px] leading-[32px]">{timeline.company.position}</p>
            <p class="descr font-[400] text-[12px] leading-[14.52px]">{timeline.company.duration}</p>
          </div>
        </div>
      </div>
      {/each}
    </div>
  </SectionWrapper>