<script setup>
import { format } from "date-fns";
import { onMounted, ref } from "vue";
const supabase = useSupabaseClient();
const items = ref([]);

onMounted(async () => {
  const { data, error } = await supabase.from("blogs").select("*");
  if (error) {
    console.error(error);
  } else {
    items.value = data.map((item) => {
      return {
        ...item,
        created_at: format(new Date(item.created_at), "yyyy-MM-dd"),
      };
    });
  }
});
</script>
<template>
  <div>
    <Head>
      <Title>Home | Portfolio</Title>
      <Meta name="description" content="My personal blog and porfolio" />
    </Head>
    <section class="relative">
      <img
        class="lg:absolute lg:w-1/3 lg:right-0 lg:top-0"
        src="~/assets/images/my-photo.jpg"
        alt="shaungbhone"
      />
      <div class="container">
        <p
          class="md:text-5xl/snug xl:text-6xl/snug text-2xl/snug font-extralight lg:w-1/2 xl:pt-32 py-12"
        >
          <span class="p-1 italic">Digital </span>
          <span class="italic">change-maker</span> <br />
          seeking <span class="bg-cyan-300">next opportunity</span> <br />
          to make an <span class="font-bold">impact</span>. <br />
          <span class="italic">Take me on >>></span>
        </p>
      </div>
    </section>
    <section class="xl:mt-60 lg:mt-28 relative">
      <h1 class="md:text-6xl text-4xl font-thin container">
        My 4-Year Odyssey in <span class="font-bold">Code</span>
      </h1>
      <div
        class="w-3/5 bg-cyan-300 md:h-40 h-20 absolute left-0 top-6 -z-10"
      ></div>
    </section>
    <section class="container xl:px-96 md:mt-44 mt-24">
      <p class="font-normal text-lg leading-loose">
        I've been learning to code for 4 years, after switching careers. I
        started with HTML, CSS, and javascript. And I made a simple static
        project called Yangon Night. But have really found a passion for backend
        development. So I started with PHP with the laravel framework and I got
        a job at a web agency called Digital Dots as a junior web developer. And
        then, I have done many projects here and built many laravel projects.
        Sometimes, contributing the packages like filament admin and voyager
        admin, and others. However, I need to level up my skill and change to
        another company as a full-stack developer called MINT.
      </p>
      <p class="md:mt-14 mt-5 text-2xl/loose md:text-4xl/relaxed font-thin">
        <span>Content Strategy</span>&nbsp;
        <span class="p-1 bg-gray-900 text-white">Writing</span> <br />
        <span class="p-1 bg-gray-300">Project Management</span><br />
        <span class="p-1 bg-gray-900 text-white">Laravel</span>&nbsp;
        <span>Nodejs</span> <br />
        <span class="p-1 bg-gray-300">PostgreSQL</span>&nbsp;
        <span class="p-1 bg-gray-900 text-white">Tailwind</span> <br />
        <span>Creative Initiatives</span>
      </p>
      <div class="mt-20">
        <a href="/pdf/latest-resume.pdf" download class="primary-btn"
          >Download Resume</a
        >
      </div>
    </section>
    <section class="md:mt-10 mt-28">
      <div class="flex">
        <div class="xl:w-3/5 lg:w-1/2 hidden md:block"></div>
        <div class="xl:w-2/5 lg:w-1/2 w-full">
          <img
            class="grayscale"
            src="~/assets/images/sb-looks-laptop.jpg"
            alt="shaungbhone"
          />
        </div>
      </div>
    </section>
    <section>
      <div class="container md:-mt-36 -mt-20">
        <div
          class="bg-gray-300 xl:ml-48 xl:mr-80 lg:mr-56 lg:py-16 lg:px-24 px-5 py-7 space-y-10 lg:space-y-16 relative"
        >
          <h1 class="lg:text-6xl text-4xl font-thin leading-tight">
            I <span class="font-bold">advise</span> companies <br />
            and my clients in initiatives.
          </h1>
          <p class="font-normal text-lg leading-loose">
            I am dedicated to helping companies and clients navigate the
            ever-evolving world of technology and software development. With my
            deep expertise in coding, programming languages, and software
            architecture, I provide valuable advice and guidance to ensure
            successful software initiatives.
          </p>
          <p class="font-normal text-lg leading-loose">
            One of my key roles as a developer advisor is to assist companies in
            selecting the right technologies and platforms for their software
            projects. This involves understanding their business requirements,
            evaluating different technologies based on factors such as
            scalability, performance, and security, and recommending the most
            suitable options.
          </p>
          <div>
            <NuxtLink class="primary-btn" to="/contact">Get in touch</NuxtLink>
          </div>
          <div
            class="bg-cyan-300 w-24 h-[96%] absolute top-0 -right-12 hidden lg:block"
          ></div>
        </div>
      </div>
    </section>
    <section class="mt-24 relative">
      <h1 class="md:text-6xl text-4xl font-thin container">
        <span>Clients &</span> <br />
        <span class="font-bold">Collaborations</span>
      </h1>
      <div
        class="w-3/5 bg-cyan-300 h-40 absolute left-0 lg:top-24 top-10 -z-10"
      ></div>
    </section>
    <section class="container mt-48">
      <div class="bg-white py-12 sm:py-16">
        <div class="mx-auto max-w-7xl px-6 lg:px-8">
          <div
            class="mx-auto grid max-w-lg items-center gap-x-8 gap-y-10 sm:max-w-xl sm:grid-cols-6 sm:gap-x-10 lg:mx-0 lg:max-w-none lg:grid-cols-5"
          >
            <a
              href="https://msmemm.org/en"
              target="_blank"
              rel="noopener noreferrer"
            >
              <img
                class="col-span-2 max-h-12 w-full object-contain lg:col-span-1"
                src="~/assets/images/msme.png"
                alt="MSME"
                width="158"
                height="48"
              />
            </a>
            <a
              href="https://digitaldots.com.mm/"
              target="_blank"
              rel="noopener noreferrer"
            >
              <img
                class="col-span-2 max-h-12 w-full object-contain lg:col-span-1"
                src="~/assets/images/dd.png"
                alt="MSME"
                width="158"
                height="48"
              />
            </a>
            <a
              href="https://www.mintasia.co"
              target="_blank"
              rel="noopener noreferrer"
            >
              <img
                class="col-span-2 max-h-12 w-full object-contain lg:col-span-1"
                src="~/assets/images/mint-logo.png"
                alt="mint"
                width="158"
                height="48"
              />
            </a>
            <a
              href="https://key-persons.jp/"
              target="_blank"
              rel="noopener noreferrer"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="158"
                height="48"
                viewBox="0 0 425 113"
                fill="none"
                class="col-span-2 max-h-12 w-full object-contain lg:col-span-1"
              >
                <g clip-path="url(#clip0_501:10789)">
                  <path
                    d="M311.91 62.3917C312.785 66.023 314.535 67.4583 318.352 67.4583C321.953 67.4583 324.206 65.9225 324.206 63.4395C324.211 62.9285 324.098 62.4233 323.877 61.9629C323.655 61.5024 323.331 61.0991 322.929 60.7842C322.011 60.0953 321.709 60.0522 317.807 59.0906C315.372 58.6536 313.007 57.8909 310.776 56.8228C309.46 56.1871 308.354 55.186 307.591 53.939C306.828 52.692 306.439 51.2517 306.472 49.7899C306.419 48.0387 306.921 46.3156 307.907 44.8669C309.915 42.1112 313.23 40.7333 317.678 40.7333C321.681 40.7333 324.851 41.7954 326.846 43.8048C328.205 45.2649 329.121 47.082 329.486 49.0436L323.044 49.9478C322.513 47.0773 320.848 45.7568 317.678 45.7568C314.507 45.7568 312.598 47.1921 312.598 49.4598C312.596 49.9656 312.728 50.463 312.98 50.9016C313.232 51.3401 313.595 51.7043 314.033 51.9572C315.59 52.6909 317.234 53.2216 318.926 53.536C323.905 54.6986 325.899 55.445 327.535 56.7654C328.506 57.5465 329.274 58.5509 329.774 59.693C330.273 60.835 330.49 62.0809 330.404 63.3247C330.385 65.5472 329.536 67.6823 328.022 69.3098C325.77 71.5775 322.283 72.7401 317.979 72.7401C312.943 72.7401 309.184 71.1039 307.089 68.0324C306.135 66.6131 305.49 65.0092 305.195 63.3247L311.91 62.3917Z"
                    fill="#323333"
                  />
                  <path
                    d="M334.206 56.7941C334.206 46.9481 339.874 40.6615 348.755 40.6615C357.637 40.6615 363.203 46.905 363.203 56.6793C363.203 66.4536 357.464 72.9267 348.856 72.9267C339.874 72.9267 334.206 66.6832 334.206 56.7941ZM340.505 56.7941C340.505 63.2959 343.633 67.3147 348.712 67.3147C353.791 67.3147 356.905 63.3533 356.905 56.8946C356.905 50.077 353.935 46.1587 348.755 46.1587C343.576 46.1587 340.505 50.2349 340.505 56.7941Z"
                    fill="#323333"
                  />
                  <path
                    d="M406.405 62.3917C407.237 65.9943 409.031 67.4296 412.847 67.4296C416.449 67.4296 418.701 65.8938 418.701 63.4108C418.706 62.8998 418.594 62.3946 418.372 61.9342C418.151 61.4737 417.826 61.0704 417.424 60.7555C416.506 60.0666 416.205 60.0235 412.302 59.0619C409.872 58.6256 407.512 57.8627 405.286 56.7941C403.971 56.157 402.866 55.1556 402.103 53.9089C401.34 52.6622 400.951 51.2227 400.982 49.7612C400.955 48.0006 401.488 46.277 402.502 44.8382C404.497 42.0825 407.811 40.7046 412.259 40.7046C416.262 40.7046 419.433 41.7667 421.427 43.7761C422.787 45.2362 423.702 47.0533 424.067 49.0149L417.625 49.9191C417.094 47.0486 415.43 45.7281 412.259 45.7281C409.088 45.7281 407.18 47.1634 407.18 49.4311C407.186 49.9455 407.331 50.4487 407.599 50.8881C407.866 51.3274 408.247 51.6868 408.701 51.9285C410.251 52.6654 411.891 53.1962 413.579 53.5073C418.558 54.6699 420.552 55.4162 422.188 56.7367C423.158 57.5186 423.926 58.5231 424.425 59.665C424.925 60.8068 425.142 62.0524 425.057 63.2959C425.033 65.5202 424.179 67.655 422.661 69.2811C420.423 71.5488 416.922 72.7114 412.618 72.7114C407.596 72.7114 403.837 71.0752 401.728 68.0037C400.78 66.5812 400.135 64.9787 399.834 63.2959L406.405 62.3917Z"
                    fill="#323333"
                  />
                  <path
                    d="M124.181 36.6284C124.138 34.3479 124.282 32.0678 124.612 29.8108H117.438C117.728 32.0713 117.858 34.3496 117.825 36.6284V65.0901C117.852 67.3735 117.722 69.6562 117.438 71.922H124.612C124.274 69.6611 124.13 67.3755 124.181 65.0901V36.6284Z"
                    fill="#323333"
                  />
                  <path
                    d="M193.697 66.023L196.911 58.5739L192.851 47.7805C192.02 45.7948 191.386 43.7325 190.957 41.6232H183.539C184.113 42.7858 184.17 42.9436 186.308 48.1824L193.697 66.023Z"
                    fill="#323333"
                  />
                  <path
                    d="M206.036 41.6232C205.615 43.7591 204.99 45.8497 204.171 47.8667L193.783 73.9457C193.496 74.7237 192.978 75.3951 192.298 75.8697C191.618 76.3444 190.81 76.5996 189.981 76.601C188.787 76.5725 187.617 76.2627 186.566 75.6968L185.433 81.725C187.112 82.1231 188.829 82.3349 190.555 82.3565C195.103 82.3565 197.973 80.505 199.537 76.4862L210.671 48.1824C212.105 44.4794 213.009 42.3121 213.296 41.6232H206.036Z"
                    fill="#323333"
                  />
                  <path
                    d="M223.268 41.6232H216.769C217.025 43.9776 217.14 46.3453 217.113 48.7135V75.2519C217.125 77.5863 217.01 79.9197 216.769 82.2417H223.656C223.396 79.9019 223.281 77.5484 223.311 75.1944L223.268 41.6232Z"
                    fill="#323333"
                  />
                  <path
                    d="M374.61 41.4509H368.211C368.195 41.4503 368.179 41.4534 368.165 41.4601C368.15 41.4669 368.137 41.477 368.127 41.4896C368.118 41.5023 368.111 41.5171 368.108 41.5328C368.105 41.5485 368.106 41.5648 368.111 41.5801C368.386 43.8177 368.506 46.0717 368.469 48.3259V64.9465C368.508 67.2012 368.383 69.4557 368.096 71.6923C368.099 71.7234 368.111 71.7528 368.132 71.7761C368.153 71.7994 368.18 71.8154 368.211 71.8215H374.983C375 71.8216 375.016 71.8183 375.031 71.8116C375.046 71.805 375.059 71.7952 375.07 71.783C375.081 71.7707 375.089 71.7563 375.094 71.7407C375.099 71.7251 375.1 71.7086 375.098 71.6923C374.822 69.4547 374.697 67.2009 374.725 64.9465V41.6232C374.732 41.6042 374.734 41.584 374.731 41.564C374.729 41.5441 374.722 41.525 374.711 41.5083C374.7 41.4915 374.685 41.4776 374.667 41.4677C374.65 41.4577 374.63 41.452 374.61 41.4509V41.4509Z"
                    fill="#323333"
                  />
                  <path
                    d="M289.154 46.5318V41.6232H282.525C282.811 43.903 282.926 46.2011 282.869 48.4982V65.047C282.88 67.3432 282.765 69.6383 282.525 71.922H289.498C289.252 69.6388 289.137 67.3434 289.154 65.047C289.154 65.047 289.168 46.5175 289.154 46.5318Z"
                    fill="#323333"
                  />
                  <path
                    d="M146.435 65.2049L134.038 47.0055L144.484 35.4228C146.622 33.0402 148.243 31.3466 149.649 29.8108H140.423C139.375 31.6755 138.098 33.4017 136.621 34.9491L127.467 45.2545V53.7513L129.504 51.5553L139.175 66.3675C140.322 68.1503 141.353 70.0057 142.26 71.922H151.285C149.539 69.7789 147.92 67.5361 146.435 65.2049V65.2049Z"
                    fill="#323333"
                  />
                  <path
                    d="M173.811 64.7312C173.057 65.5868 172.124 66.2664 171.079 66.722C170.033 67.1776 168.901 67.3981 167.761 67.368C166.621 67.3379 165.502 67.0579 164.482 66.5477C163.462 66.0376 162.567 65.3097 161.859 64.4155C161.555 64.001 161.291 63.5589 161.07 63.095C160.442 61.6376 160.096 60.0742 160.051 58.4877C159.843 56.7103 159.891 54.9121 160.195 53.1485C160.496 51.8854 161.357 48.2685 164.413 46.7615C165.385 46.2961 166.449 46.0558 167.526 46.0582C168.505 46.0002 169.485 46.1593 170.395 46.5241C171.305 46.8888 172.124 47.4502 172.792 48.1681C174.047 49.5797 174.803 51.365 174.944 53.249H163.566V58.4877H181.286C181.186 57.2678 181.186 57.0525 181.186 57.0525C181.188 54.3047 180.702 51.5783 179.751 49.0005C178.886 46.4901 177.239 44.3236 175.051 42.8199C172.863 41.3162 170.251 40.5546 167.598 40.6472C159.262 40.6472 153.838 47.0485 153.838 56.8372C153.838 66.6258 159.305 72.9697 167.942 72.9697C169.809 73.0346 171.668 72.7051 173.399 72.0027C175.129 71.3004 176.692 70.2409 177.986 68.8935C179.28 67.478 180.288 65.8259 180.956 64.0279L175.217 62.0185C174.931 63.0063 174.453 63.928 173.811 64.7312V64.7312Z"
                    fill="#323333"
                  />
                  <path
                    d="M270.114 64.7312C269.36 65.5868 268.427 66.2664 267.382 66.722C266.337 67.1776 265.204 67.3981 264.064 67.368C262.925 67.3379 261.805 67.0579 260.785 66.5477C259.766 66.0376 258.87 65.3097 258.162 64.4155C257.859 64.001 257.594 63.5589 257.373 63.095C256.745 61.6376 256.399 60.0742 256.354 58.4877C256.146 56.7103 256.194 54.9121 256.498 53.1485C256.799 51.8854 257.66 48.2685 260.716 46.7615C261.688 46.2961 262.752 46.0558 263.83 46.0582C264.809 46.0002 265.788 46.1593 266.698 46.5241C267.609 46.8888 268.427 47.4502 269.095 48.1681C270.351 49.5797 271.107 51.365 271.248 53.249H259.87V58.4877H277.589C277.489 57.2678 277.489 57.0525 277.489 57.0525C277.491 54.3047 277.005 51.5783 276.054 49.0005C275.189 46.4901 273.542 44.3236 271.354 42.8199C269.167 41.3162 266.554 40.5546 263.901 40.6472C255.565 40.6472 250.142 47.0485 250.142 56.8372C250.142 66.6258 255.608 72.9697 264.246 72.9697C266.112 73.0346 267.971 72.7051 269.702 72.0027C271.433 71.3004 272.996 70.2409 274.289 68.8935C275.583 67.478 276.592 65.8259 277.259 64.0279L271.52 62.0185C271.234 63.0063 270.756 63.928 270.114 64.7312V64.7312Z"
                    fill="#323333"
                  />
                  <path
                    d="M242.48 44.4937C241.29 43.2493 239.846 42.2749 238.247 41.636C236.648 40.9972 234.931 40.709 233.211 40.7907C230.974 40.7014 228.761 41.2811 226.855 42.4556V48.4551C228.273 47.1655 230.119 46.4493 232.035 46.4457C236.971 46.4457 239.998 50.3066 239.998 56.4927C239.998 62.6788 237.014 66.6545 232.236 66.6545C230.253 66.6722 228.335 65.9507 226.855 64.6308V70.5872C228.748 71.7027 230.915 72.2647 233.111 72.209C241.418 72.209 246.34 66.3387 246.34 56.5932C246.297 51.34 245.034 47.3643 242.48 44.4937Z"
                    fill="#323333"
                  />
                  <path
                    d="M298.336 40.9773C296.255 40.9034 294.2 41.4586 292.439 42.5705V48.7996C293.705 47.8699 295.247 47.3945 296.816 47.4504C298.287 47.4916 299.742 47.7778 301.12 48.2972L302.87 41.6232C301.383 41.2631 299.865 41.0468 298.336 40.9773Z"
                    fill="#323333"
                  />
                  <path
                    d="M394.568 64.9465V52.2443C394.568 48.6991 394.08 46.5893 392.904 44.8382C391.968 43.5126 390.703 42.4539 389.234 41.7667C387.764 41.0796 386.141 40.7877 384.524 40.9199C382.484 40.8182 380.459 41.3172 378.699 42.3552V48.0963C379.935 46.9782 381.539 46.3548 383.204 46.3453C384.038 46.2869 384.871 46.4613 385.611 46.849C386.35 47.2368 386.968 47.8227 387.394 48.5413C388.069 49.9931 388.356 51.5955 388.226 53.1916V64.9465C388.239 67.1995 388.129 69.4514 387.896 71.6924C387.894 71.7086 387.896 71.7251 387.9 71.7407C387.905 71.7564 387.913 71.7708 387.924 71.783C387.935 71.7952 387.949 71.805 387.963 71.8117C387.978 71.8183 387.995 71.8217 388.011 71.8215H394.826C394.858 71.818 394.887 71.8028 394.908 71.779C394.93 71.7551 394.941 71.7243 394.941 71.6924C394.647 69.4564 394.522 67.2013 394.568 64.9465Z"
                    fill="#323333"
                  />
                  <path
                    d="M92.2142 86.6623L84.6529 67.6161C84.5708 67.41 84.4488 67.2222 84.2938 67.0636C84.1387 66.9049 83.9538 66.7786 83.7497 66.6919C83.5456 66.6051 83.3263 66.5597 83.1045 66.5582C82.8828 66.5567 82.6629 66.5992 82.4577 66.6832L78.8133 68.1185L63.0306 74.4624L58.7979 63.6548C59.0739 63.5054 59.3026 63.2817 59.4579 63.0089L62.3275 57.5261L76.0441 65.2766C76.2442 65.3942 76.4661 65.4697 76.6963 65.4986C76.9266 65.5275 77.1603 65.5091 77.3832 65.4447C77.6061 65.3802 77.8135 65.271 77.9928 65.1236C78.172 64.9763 78.3194 64.7939 78.4259 64.5877L80.3485 61.2291C80.4655 61.0281 80.5402 60.8053 80.5681 60.5744C80.5959 60.3435 80.5764 60.1093 80.5105 59.8862C80.4447 59.6631 80.334 59.4558 80.1853 59.2771C80.0365 59.0983 79.8528 58.9518 79.6455 58.8466L65.5988 51.0099L71.7398 39.3841C71.8442 39.1845 71.9081 38.9662 71.9278 38.7417C71.9476 38.5173 71.9227 38.2912 71.8547 38.0764C71.7867 37.8616 71.6769 37.6624 71.5315 37.4902C71.3862 37.3181 71.2083 37.1764 71.008 37.0733L67.5789 35.2792C67.3797 35.1728 67.1613 35.1073 66.9365 35.0865C66.7116 35.0658 66.4849 35.0902 66.2697 35.1584C66.0545 35.2266 65.855 35.3372 65.6831 35.4837C65.5113 35.6301 65.3704 35.8095 65.2688 36.0112L55.2683 55.0718L48.8835 39.1401L64.6662 32.7818L68.2532 31.3466C68.6752 31.1743 69.0125 30.8429 69.1923 30.424C69.3722 30.0051 69.3801 29.5322 69.2145 29.1075L67.7797 25.5193L61.1223 8.82697L59.6875 5.23876C59.6013 5.02407 59.4728 4.82894 59.3097 4.66502C59.1465 4.5011 58.9519 4.37174 58.7377 4.28467C58.5234 4.1976 58.2938 4.1546 58.0626 4.15823C57.8314 4.16187 57.6032 4.21207 57.3918 4.30583L53.8048 5.74111L27.5768 16.2761L23.9898 17.7114C23.7798 17.795 23.5884 17.9195 23.4268 18.0777C23.2652 18.2359 23.1366 18.4246 23.0485 18.6329C22.9604 18.8412 22.9146 19.0649 22.9136 19.2911C22.9126 19.5173 22.9566 19.7414 23.0429 19.9504L24.4777 23.5243L31.1638 40.1879L32.5986 43.7617C32.6793 43.9727 32.8013 44.1653 32.9575 44.3283C33.1137 44.4914 33.3009 44.6215 33.5081 44.7111C33.7153 44.8007 33.9383 44.848 34.1641 44.8501C34.3898 44.8522 34.6137 44.8091 34.8225 44.7234L38.4095 43.2881L42.0969 41.8528L68.7697 108.637C68.9388 109.054 69.2658 109.388 69.6796 109.565C70.0934 109.742 70.5606 109.749 70.9793 109.584L74.6093 108.149C75.0256 107.982 75.359 107.658 75.5365 107.246C75.714 106.835 75.7211 106.369 75.5563 105.953L71.8402 96.6806L89.6029 89.5042L91.2816 88.8296C91.6883 88.6606 92.0132 88.3398 92.1873 87.9352C92.3614 87.5305 92.3711 87.074 92.2142 86.6623V86.6623ZM41.3221 34.3032C40.7958 34.5178 40.2322 34.626 39.6638 34.6215C39.0954 34.617 38.5336 34.5 38.0107 34.2771C37.4878 34.0543 37.0141 33.73 36.6172 33.3231C36.2202 32.9162 35.9077 32.4347 35.6978 31.9063L33.5025 26.4235C33.2872 25.8988 33.1777 25.3366 33.1802 24.7694C33.1828 24.2022 33.2973 23.641 33.5173 23.1182C33.7373 22.5954 34.0584 22.1212 34.4621 21.7229C34.8659 21.3246 35.3443 21.01 35.8699 20.7972L50.9496 14.7547C51.4812 14.5398 52.0504 14.4333 52.6237 14.4414C53.197 14.4496 53.7629 14.5723 54.2882 14.8023C54.8135 15.0322 55.2875 15.3649 55.6825 15.7806C56.0775 16.1964 56.3855 16.6869 56.5883 17.2234L58.8266 22.6344C59.0407 23.1618 59.1482 23.7265 59.1427 24.2957C59.1373 24.8649 59.0191 25.4274 58.7949 25.9506C58.5707 26.4739 58.2451 26.9474 57.8368 27.3439C57.4285 27.7405 56.9456 28.0521 56.4162 28.2607L41.3221 34.3032ZM65.7136 81.2513L79.9468 75.5102L83.4046 84.1219L69.1715 89.863L65.7136 81.2513Z"
                    fill="#ADD37F"
                  />
                </g>
                <defs>
                  <clipPath id="clip0_501:10789">
                    <rect width="425" height="112.096" fill="white" />
                  </clipPath>
                </defs>
              </svg>
            </a>
            <a
              href="https://www.umapoi.jp/"
              target="_blank"
              rel="noopener noreferrer"
            >
              <img
                class="col-span-2 max-h-12 w-full object-contain lg:col-span-1"
                src="~/assets/images/umapoi.png"
                alt="Umapoi"
                width="158"
                height="48"
              />
            </a>
          </div>
          <div class="block md:flex mt-10 justify-center space-x-12">
            <a href="https://www.edventuremm.com" target="_blank">
              <img
                class="col-span-2 max-h-12 w-full object-contain lg:col-span-1"
                src="~/assets/images/edv.png"
                alt="Edventure Education"
                width="158"
                height="48"
              />
            </a>
            <a href="http://digify-me.com" target="_blank">
              <img
                class="col-span-2 max-h-12 w-full object-contain lg:col-span-1"
                src="~/assets/images/digify-me-logo-red.png"
                alt="Digifyme"
                width="158"
                height="48"
              />
            </a>
          </div>
        </div>
      </div>
    </section>
    <section class="mt-16">
      <div class="bg-white py-14">
        <div class="container">
          <div class="mx-auto lg:mx-0 text-center">
            <h2
              class="font-thin tracking-tight text-gray-900 text-3xl md:text-6xl"
            >
              Recent <span class="font-bold">Blog</span> Posts
            </h2>
            <p class="mt-5 text-lg leading-8 text-gray-600">
              Knowledge is not just power, it's also the key to progress and
              growth.
            </p>
          </div>
          <div
            class="mx-auto mt-10 grid max-w-2xl grid-cols-1 gap-x-8 gap-y-16 border-t border-gray-200 pt-10 sm:mt-16 sm:pt-16 lg:mx-0 lg:max-w-none lg:grid-cols-3"
          >
            <div v-for="item in items" :key="item.id">
              <article
                class="flex max-w-xl flex-col items-start justify-between"
              >
                <div class="flex items-center gap-x-4 text-xs">
                  <time datetime="2020-03-16" class="text-gray-500">{{
                    item.created_at
                  }}</time>
                  <a
                    href="#"
                    class="relative z-10 rounded-full bg-gray-50 px-3 py-1.5 font-medium text-gray-600 hover:bg-gray-100"
                    >{{ item.tag }}</a
                  >
                </div>
                <div class="group relative">
                  <h3
                    class="mt-3 text-lg font-semibold leading-6 text-gray-900 group-hover:text-gray-600"
                  >
                    <NuxtLink :to="`/blog/${item.id}`">
                      <span class="absolute inset-0"></span>
                      {{ item.title }}
                    </NuxtLink>
                  </h3>
                  <p class="mt-5 line-clamp-3 text-sm leading-6 text-gray-600">
                    {{ item.content }}
                  </p>
                </div>
              </article>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>
