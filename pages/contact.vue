<template>
  <div>
    <Head>
      <Title>Contact | Portfolio</Title>
    </Head>
    <section class="mt-10 relative">
      <h1 class="md:text-6xl text-4xl font-thin container">
        <span class="font-bold">Contact</span>
      </h1>
      <div
        class="w-3/5 bg-cyan-300 md:h-40 h-20 absolute left-0 top-6 -z-10"
      ></div>
    </section>
    <section>
      <div class="isolate px-6 py-24 sm:py-32 lg:px-8">
        <div
          class="absolute inset-x-0 top-[-10rem] -z-10 transform-gpu overflow-hidden blur-3xl sm:top-[-20rem]"
          aria-hidden="true"
        ></div>
        <form action="#" method="POST" class="mx-auto mt-16 max-w-xl sm:mt-20">
          <div class="grid grid-cols-1 gap-x-8 gap-y-6 sm:grid-cols-2">
            <div class="sm:col-span-2">
              <label
                for="name"
                class="block text-sm font-semibold leading-6 text-gray-900"
                >Name</label
              >
              <div class="mt-2.5">
                <input
                  type="text"
                  name="name"
                  id="name"
                  autocomplete="organization"
                  class="block w-full rounded-md border-0 px-3.5 py-2 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-cyan-300 sm:text-sm sm:leading-6"
                />
              </div>
            </div>
            <div class="sm:col-span-2">
              <label
                for="email"
                class="block text-sm font-semibold leading-6 text-gray-900"
                >Email</label
              >
              <div class="mt-2.5">
                <input
                  type="email"
                  name="email"
                  id="email"
                  autocomplete="email"
                  class="block w-full rounded-md border-0 px-3.5 py-2 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-cyan-300 sm:text-sm sm:leading-6"
                />
              </div>
            </div>
            <div class="sm:col-span-2">
              <label
                for="message"
                class="block text-sm font-semibold leading-6 text-gray-900"
                >Message</label
              >
              <div class="mt-2.5">
                <textarea
                  name="message"
                  id="message"
                  rows="4"
                  class="block w-full rounded-md border-0 px-3.5 py-2 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-cyan-300 sm:text-sm sm:leading-6"
                ></textarea>
              </div>
            </div>
          </div>
          <div class="mt-10">
            <button
              type="submit"
              class="block w-full rounded-md bg-cyan-300 px-3.5 py-2.5 text-center text-sm font-semibold text-white shadow-sm hover:bg-cyan-300 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-cyan-300"
            >
              Let's talk
            </button>
          </div>
        </form>
      </div>
    </section>
  </div>
</template>
