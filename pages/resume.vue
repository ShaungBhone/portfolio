<template>
  <div>
    <Head>
      <Title>Resume | Portfolio</Title>
    </Head>
    <section class="mt-10 relative">
      <h1 class="md:text-6xl text-4xl font-thin container">
        <span class="font-bold">Resume</span>
      </h1>
      <div
        class="w-3/5 bg-cyan-300 md:h-40 h-20 absolute left-0 top-6 -z-10"
      ></div>
    </section>
    <section class="container">
      <div class="lg:px-64 lg:pt-52 lg:pb-40 lg:mt-10 md:mt-44 mt-20">
        <h1 class="font-thin md:text-5xl text-2xl">
          <span class="font-bold">Professional</span> Summary
        </h1>
        <p class="mt-10 text-lg/loose">
          Driven 4-year experienced web developer with a passion for crafting
          visually appealing and user-friendly websites. Seeking a challenging
          role where I can utilize and contribute my coding skills, creativity,
          and problem-solving abilities to deliver cutting-edge web solutions
          that meet client needs and enhance user experiences.
        </p>
        <div class="mt-20">
          <a href="/pdf/latest-resume.pdf" download class="primary-btn"
            >Download Resume</a
          >
        </div>
      </div>
    </section>
    <section class="mt-36 lg:mt-10 relative">
      <h1 class="md:text-6xl container text-3xl font-thin">
        <span class="font-bold">Skills</span>
      </h1>
      <div
        class="w-2/5 bg-cyan-300 md:h-40 h-20 absolute left-0 top-5 -z-10"
      ></div>
      <div
        class="lg:px-60 lg:pt-48 lg:pb-40 lg:mt-10 md:mt-44 mt-28 px-10 container"
      >
        <p class="font-bold lg:text-3xl/loose text-xl/loose">
          <span class="p-1 bg-gray-300">Writing</span>&nbsp;
          <span class="p-1 bg-gray-300">Project Management</span>&nbsp;
          <span class="p-1 bg-gray-300">Laravel</span>&nbsp;
          <span class="p-1 bg-gray-300">Nodejs</span>&nbsp;
          <span class="p-1 bg-gray-300">Vuejs</span>&nbsp;
          <span class="p-1 bg-gray-300">React</span>&nbsp;
          <span class="p-1 bg-gray-300">Pest</span>&nbsp;
          <span class="p-1 bg-gray-300">Livewire</span>&nbsp;
          <span class="p-1 bg-gray-300">Tailwind</span>&nbsp;
          <span class="p-1 bg-gray-300">PostgreSQL</span>&nbsp;
          <span class="p-1 bg-gray-300">MySQL</span>&nbsp;
          <span class="p-1 bg-gray-300">Docker</span>&nbsp;
          <span class="p-1 bg-gray-300">GraphQL</span>&nbsp;
          <span class="p-1 bg-gray-300">AWS</span>&nbsp;
        </p>
      </div>
    </section>
    <section class="mt-10 relative">
      <h1 class="md:text-6xl text-3xl font-thin container">
        <span class="font-thin"
          >Work <span class="font-bold">Experiences</span></span
        >
      </h1>
      <div
        class="w-2/5 bg-cyan-300 md:h-40 h-20 absolute left-0 top-5 -z-10"
      ></div>
      <div
        class="lg:px-64 lg:pt-52 lg:pb-32 space-y-8 container mt-24 lg:mb-0 mb-16 md:mt-36 lg:mt-10"
      >
        <article class="flex max-w-xl flex-col items-start justify-between">
          <div class="flex items-center gap-x-4 text-sm">
            <time class="text-gray-500">May 2022 - present</time>
            <a
              href="#"
              class="relative z-10 rounded-full bg-[#65E0CC] px-3 py-1.5 font-medium text-gray-900 hover:bg-gray-100"
              >Mint</a
            >
          </div>
          <div class="group relative">
            <h3
              class="mt-3 text-xl font-semibold leading-6 text-gray-900 group-hover:text-gray-600"
            >
              <NuxtLink href="https://www.mintasia.co">
                <span class="absolute inset-0"></span>
                Team Lead
              </NuxtLink>
            </h3>
            <p class="mt-5 line-clamp-3 text-md leading-7 text-gray-600">
              Leading development projects: working closely with project
              managers and collaborating with other team members.
            </p>
          </div>
        </article>
        <article class="flex max-w-xl flex-col items-start justify-between">
          <div class="flex items-center gap-x-4 text-sm">
            <time class="text-gray-500">Mar 2020 - June 2022</time>
            <NuxtLink
              href="https://www.digitaldots.com.mm/"
              class="relative z-10 rounded-full bg-[#641C55] px-3 py-1.5 font-medium text-white hover:bg-gray-100 hover:text-gray-900"
              >Digital Dots
            </NuxtLink>
          </div>
          <div class="group relative">
            <h3
              class="mt-3 text-xl font-semibold leading-6 text-gray-900 group-hover:text-gray-600"
            >
              <a href="#">
                <span class="absolute inset-0"></span>
                Junior Developer
              </a>
            </h3>
            <p class="mt-5 line-clamp-3 text-md leading-7 text-gray-600">
              Developing and maintaining WordPress websites, including
              installing and configuring WordPress, creating and customizing
              themes, and installing and configuring plugins.
            </p>
          </div>
        </article>
        <article class="flex max-w-xl flex-col items-start justify-between">
          <div class="flex items-center gap-x-4 text-sm">
            <time class="text-gray-500">May 2022 - present</time>
            <NuxtLink
              href="https://www.upwork.com/"
              class="relative z-10 rounded-full bg-[#6fda44] px-3 py-1.5 font-medium text-white hover:bg-gray-100 hover:text-gray-900"
              >Upwork
            </NuxtLink>
          </div>
          <div class="group relative">
            <h3
              class="mt-3 text-xl font-semibold leading-6 text-gray-900 group-hover:text-gray-600"
            >
              <a href="#">
                <span class="absolute inset-0"></span>
                Freelancer
              </a>
            </h3>
            <p class="mt-5 line-clamp-3 text-md leading-7 text-gray-600">
              Communicating with international clients for their specific
              requirements.
            </p>
          </div>
        </article>
      </div>
    </section>
  </div>
</template>
