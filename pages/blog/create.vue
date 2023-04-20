<script setup>
const supabase = useSupabaseClient();
const title = ref("");
const tag = ref("");
const content = ref("");
const errors = ref([]);
const successMessage = ref("");
const loading = ref(false);

const create = async () => {
  loading.value = true;
  const user = useSupabaseUser();
  try {
    const { error } = await supabase
      .from("blogs")
      .insert(
        { title: title.value, tag: tag.value, content: content.value },
        { returning: "minimal" }
      )
      .eq("id", user.value.id)
      .single();
    if (error) throw error;
    successMessage.value = "Successfully created!";
  } catch (error) {
    errors.value = Object.values(error).flat();
    title.value = "";
    tag.value = "";
    content.value = "";
  } finally {
    loading.value = false;
  }
};
</script>

<template>
  <div>
    <Head>
      <Title>Blog | Portfolio</Title>
    </Head>
    <form @submit.prevent="create" class="container max-w-3xl mb-10">
      <div class="space-y-4">
        <div>
          <label
            for="title"
            class="block text-sm font-medium leading-6 text-gray-900"
            >Title</label
          >
          <div class="mt-2">
            <input
              v-model="title"
              type="text"
              name="title"
              id="title"
              autocomplete="given-name"
              class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-cyan-300 sm:text-sm sm:leading-6"
            />
          </div>
        </div>
        <div>
          <label
            for="title"
            class="block text-sm font-medium leading-6 text-gray-900"
            >Tag</label
          >
          <div class="mt-2">
            <input
              v-model="tag"
              type="text"
              name="title"
              id="title"
              autocomplete="given-name"
              class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-cyan-300 sm:text-sm sm:leading-6"
            />
          </div>
        </div>
        <div>
          <label
            for="content"
            class="block text-sm font-medium leading-6 text-gray-900"
            >Content</label
          >
          <div class="mt-2">
            <textarea
              v-model="content"
              id="content"
              name="content"
              rows="3"
              class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-cyan-300 sm:text-sm sm:leading-6"
            ></textarea>
          </div>
        </div>
      </div>
      <p class="my-4 text-md text-green-500" v-if="successMessage">
        {{ successMessage }}
      </p>
      <div class="mt-6 flex items-center justify-end gap-x-6">
        <button
          type="button"
          class="text-sm font-semibold leading-6 text-gray-900"
        >
          Cancel
        </button>
        <button
          type="submit"
          class="rounded-md bg-cyan-300 px-3 py-2 text-sm font-semibold text-white shadow-sm hover:bg-cyan-300 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-cyan-300"
        >
          Create
        </button>
      </div>
    </form>
  </div>
</template>
