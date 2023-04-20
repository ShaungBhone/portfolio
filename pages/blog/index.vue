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
      <Title>Blog | Portfolio</Title>
    </Head>
    <section class="mt-10 relative">
      <h1 class="md:text-6xl text-4xl font-thin container">
        <span class="font-bold">Blog</span>
      </h1>
      <div
        class="w-3/5 bg-cyan-300 md:h-40 h-20 absolute left-0 top-6 -z-10"
      ></div>
    </section>
    <article class="mt-10">
      <div class="py-24 sm:py-32">
        <div class="mx-auto max-w-7xl px-6 lg:px-8">
          <div
            class="mx-auto mt-10 grid max-w-2xl grid-cols-1 gap-x-8 gap-y-16 border-t border-gray-200 pt-10 sm:pt-16 lg:mx-0 lg:max-w-none lg:grid-cols-3"
          >
            <div v-for="item in items" :key="item.id">
              <article
                class="flex max-w-xl flex-col items-start justify-between"
              >
                <div class="flex items-center gap-x-4 text-xs">
                  <time datetime="2020-03-16" class="text-gray-500">
                    {{ item.created_at }}
                  </time>
                  <a
                    href="#"
                    class="relative z-10 rounded-full bg-gray-50 px-3 py-1.5 font-medium text-gray-600 hover:bg-gray-100"
                  >
                    {{ item.tag }}
                  </a>
                </div>
                <div class="group relative">
                  <h3
                    class="mt-3 text-lg font-semibold leading-6 text-gray-900 group-hover:text-gray-600"
                  >
                    <a href="#">
                      <span class="absolute inset-0"></span>
                      {{ item.title }}
                    </a>
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
    </article>
  </div>
</template>
