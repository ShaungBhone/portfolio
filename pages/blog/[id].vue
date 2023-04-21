<script setup>
import { format } from "date-fns";
const supabase = useSupabaseClient();
const route = useRoute();

const { data: blog } = await useAsyncData(
  "blogs",
  async () =>
    supabase.from("blogs").select("*").eq("id", route.params.id).single(),
  {
    transform: (result) => ({
      ...result.data,
      created_at: format(new Date(result.data.created_at), "yyyy-MM-dd"),
    }),
  }
);
</script>

<template>
  <article class="container">
    <Head>
      <Title>Blog | Portfolio</Title>
    </Head>
    <div class="mt-10 relative">
      <h1 class="md:text-6xl text-4xl font-thin container">
        <span class="font-bold">Blog</span>
      </h1>
      <div
        class="w-3/5 bg-cyan-300 md:h-40 h-20 absolute left-0 top-6 -z-10"
      ></div>
    </div>
    <div class="my-44">
      <article
        class="flex max-w-2xl mx-auto flex-col items-start justify-between"
      >
        <div class="flex items-center gap-x-4 text-xs">
          <time class="text-gray-500">{{ blog.created_at }}</time>
          <a
            href="#"
            class="relative z-10 rounded-full bg-gray-50 px-3 py-1.5 font-medium text-gray-600 hover:bg-gray-100"
            >{{ blog.tag }}</a
          >
        </div>
        <div class="group relative">
          <h3
            class="mt-3 text-2xl font-semibold leading-6 text-gray-900 group-hover:text-gray-600"
          >
            <div>
              <span class="absolute inset-0"></span>
              {{ blog.title }}
            </div>
          </h3>
          <p class="mt-5 text-lg/loose text-gray-600">
            {{ blog.content }}
          </p>
        </div>
      </article>
    </div>
  </article>
</template>
