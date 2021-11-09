<template>
  <div class="project">
    This is the project
    <div class="project-image">
      <img :src="'~/assets/' + image" />
    </div>
    <div class="project__details">
      <span class="project__details--title">
        {{ title }}
      </span>
      <span class="project__details--status">
        {{ status }}
      </span>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
    image: {
      type: String,
      required: true,
    },
    status: {
      type: String,
      required: true,
    },
  },
};
</script>