<template>
  <div class="container">
    <nav class="flex justify-between py-11">
      <div>
        <h5 class="font-bold text-lg">I'm Bhone Myint Zaw aka Shaung Bhone.</h5>
        <p>
          A <span class="bg-cyan-300 p-1">Full Stack Developer</span>, Blogger
          and Freelancer.
        </p>
      </div>
      <div class="my-auto flex">
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
