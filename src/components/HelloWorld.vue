<script setup lang="ts">
defineProps<{
  name: string
}>()
</script>

<template>
  <div class="profile-container">
    <div class="profile-image">
      <img alt="Photo" class="circular-image" src="@/assets/dog.png" width="125" height="125" />
    </div>
    <div class="profile-info">
      <h1 class="white">{{ name }}</h1>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus sed urna pulvinar, bibendum
        neque vitae, auctor ipsum. Nullam id ipsum ut nibh efficitur lobortis. Nullam condimentum
        magna quam,Sed elementum suscipit dolor, eu dapibus sem. Quisque auctor lorem
        tincidunt sollicitudin scelerisque.
      </p>
      <p>
        Proin facilisis molestie massa quis viverra. Aliquam erat volutpat. Nullam ultricies leo ut
        lacus tincidunt aliquam. Pellentesque sit amet eros id diam pellentesque lobortis in iaculis
        enim. Donec vivera, metus nec tincidunt facilisis, risus quam facilisis nibh, sed
        porttitor nunc sapien venenatis quam. Sed tristique nisi non lacus posuere, quis
        sollicitudin lectus porta.
      </p>
    </div>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

.circular-image {
  width: 150px;
  height: 150px;
  border-radius: 50%;
  object-fit: cover;
}

.profile-container {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 60px;
  padding: 15px;
  border-radius: 10px;
  margin-left: 10rem;
  margin-right: 10rem;
}

.profile-image {
  width: 150px;
  height: 150px;
  border-radius: 50%;
  object-fit: cover;
}

.profile-info {
  justify-content: center;
}
.profile-info h1 {
  margin: 0;
  font-size: 2em;
}

.profile-info p {
  margin-top: 10px;
  font-size: 1em;
  line-height: 1.5;
  text-align: justify;
}
</style>
