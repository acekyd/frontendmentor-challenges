<template>
  <nuxt-link :to="path" class="project">
    <div class="project__image">
      <img :src="'images/' + image" class="project__image--img" />
    </div>
    <div class="project__details">
      <span class="project__details--title">
        {{ title }}
      </span>
      <span class="project__details--status">
        {{ status }}
      </span>
    </div>
  </nuxt-link>
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
    path: {
      type: String,
      required: true,
    },
  },
};
</script>

<style>
.project {
  display: flex;
  flex-direction: column;
  background: #fff;
  border: rgba(100, 100, 111, 0.2) 1px solid;
  box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
  border-radius: 4px;
  text-decoration: none;
  color: #000;
}

.project:hover {
  box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
}

.project__image--img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.project__details {
  display: flex;
  justify-content: space-between;
  padding: 20px;
}

.project__details--status {
  font-size: 8px;
  padding: 4px;
  background: #eee;
  border-radius: 4px;
  display: inline-block;
  height: 10px;
}
</style>