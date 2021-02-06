<template>
  <div class="description px-4">
    <h1 class="description__name inline-block text-5xl throughlined-text font-bold text-center md:text-left">
      Роман Сарваров
    </h1>

    <h2 class="mt-2 text-center md:text-left">Full-stack разработчик</h2>

    <vue-typed-js
      :strings="skills"
      :type-speed="75"
      :back-speed="150"
      :back-delay="1000"
      :delay="1000"
      :loop="true"
      class="text-center md:text-left justify-center md:justify-start">
      <h2 class="description__skills mt-2 opacity-50 font-light">
        Знаю
        <span class="typing border-dashed border-b border-gray-300"></span>
      </h2>
    </vue-typed-js>

    <div class="mt-8 md:mt-16 text-center md:text-left">
      <a
          :href="emailMeLink"
          :class="emailMeClasses"
          class="inline-block outline-none focus:border-blue-300 focus:ring">
        <EmailSvg />
        Написать мне
      </a>
    </div>
  </div>
</template>

<script>
import EmailSvg from '@/components/svg/EmailSvg';
import config from '@/config';

export default {
  name: 'TheDescription',
  components: { EmailSvg },
  props: {
    skills: {
      type: Array,
      required: true,
    },
  },
  computed: {
    emailMeLink() {
      return `mailto:${config.myEmail}`;
    },
    emailMeClasses() {
      return [
        'bg-blue-800',
        'hover:bg-blue-900',
        'hover:shadow',
        'transition-colors',
        'text-white',
        'p-3',
        'rounded',
      ];
    },
  },
};
</script>
