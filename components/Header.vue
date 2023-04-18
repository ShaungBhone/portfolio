<template>
  <div class="container">
    <nav class="lg:flex lg:justify-between py-7 md:py-11">
      <div class="flex justify-between flex-col-reverse md:flex-row">
        <div class="mt-3 md:mt-0">
          <h5 class="font-bold text-lg">
            I'm Bhone Myint Zaw aka Shaung Bhone.
          </h5>
          <p>
            A <span class="bg-cyan-300 p-1">Full Stack Developer</span>, Blogger
            and Freelancer.
          </p>
        </div>
        <div class="my-auto lg:hidden">
          <button
            type="button"
            data-drawer-target="drawer-navigation"
            data-drawer-show="drawer-navigation"
            aria-controls="drawer-navigation"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke-width="1.5"
              stroke="currentColor"
              class="w-6 h-6"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
              />
            </svg>
          </button>
          <Sidebar />
        </div>
      </div>
      <div class="my-auto hidden lg:flex">
        <ul class="flex space-x-8">
          <li class="hover:text-gray-500 text-gray-900">
            <NuxtLink to="/">Home</NuxtLink>
          </li>
          <li class="hover:text-gray-500 text-gray-900">
            <NuxtLink to="/resume">Resume</NuxtLink>
          </li>
          <li class="hover:text-gray-500 text-gray-900">
            <NuxtLink to="/contact">Contact</NuxtLink>
          </li>
          <li class="hover:text-gray-500 text-gray-900">
            <NuxtLink to="/blog">Blog</NuxtLink>
          </li>
          <li class="hover:text-gray-500 text-gray-900">
            <NuxtLink to="https://www.facebook.com">icon</NuxtLink>
          </li>
        </ul>
      </div>
    </nav>
  </div>
</template>
