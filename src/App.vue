<template>
  <div class="min-h-screen my-auto bg-red-400 mx-auto">
    <h1 class="text-3xl font-bold underline">Hello world!</h1>

    <div
      class="
        max-w-sm
        mx-auto
        my-auto
        bg-gray-200
        px-4
        py-2
        rounded-lg
        space-y-4
      "
    >
      <div class="flex flex-col">
        <label for="name">Full Name</label>
        <BaseInput
          class=""
          type="text"
          id="name"
          v-model="event.name"
          label="Name"
        />
      </div>

      <div class="flex flex-col">
        <label for="email">Email</label>
        <BaseInput
          class=""
          type="email"
          v-model="event.email"
          label="Email"
        />
      </div>

      <div class="flex flex-col">
        <label for="password">Password</label>
        <BaseInput
          class=""
          type="password"
          v-model="event.password"
          label="Password"
        />
      </div>

      <pre>{{ JSON.stringify(event, null, 2) }}</pre>
    </div>
  </div>
</template>

<script>
import BaseInput from "./components/BaseInput.vue";
export default {
  components: {
    BaseInput,
  },
  data() {
    return {
      event: {
        name: "",
        email: "",
        password: "",
      },
    };
  },
};
</script>