<template>
  <main class="home">
    <div class="flex flex-col my-10 md:my-24">
      <div class="mx-auto">
        <div
          class="flex flex-col md:flex-row items-center transition-all duration-700 ease-in-out"
          :class="{ 'transform translate-y-24 opacity-0': loading }">
          <TheRoman class="h-1/2" />

          <div
              class="transform transition-all duration-700 ease-in-out"
              :class="{ 'transform translate-x-24 opacity-0': descriptionLoading }">
            <TheDescription
                class="mt-12 md:mt-0 md:ml-12"
                :skills="skills"
            />
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
import skills from '@/data/skills';
import TheDescription from '@/components/home/TheDescription';
import TheRoman from '@/components/home/TheRoman';

export default {
  name: 'Home',
  components: { TheRoman, TheDescription },
  data: () => ({
    loading: false,
    descriptionLoading: false,
  }),
  computed: {
    skills: () => skills,
  },
  methods: {
    async loadPage() {
      this.loading = true;
      this.descriptionLoading = true;

      await this.loadPageAction();
      await this.loadDescriptionAction();
    },
    async loadPageAction() {
      return new Promise((resolve) => {
        setTimeout(() => {
          this.loading = false;
          resolve();
        }, 500);
      });
    },
    async loadDescriptionAction() {
      return new Promise((resolve) => {
        setTimeout(() => {
          this.descriptionLoading = false;
          resolve();
        }, 500);
      });
    },
  },
  mounted() {
    this.loadPage();
  },
};
</script>
