<template>
    <div class="card">
      <header class="card-header">
        <p class="card-header-title has-text-grey">
          {{ name }}
        </p>
      </header>
      <div class="card-content image" >
        <div class="content has-text-centered image" >
          <b-image
            :class="!image ? 'filter': ''"
            :src="image || 'https://cdn.dribbble.com/users/888330/screenshots/2653750/empty_data_set.png'"
            size="is-large"
            type="is-primary"
            height="100%"
          />
        </div>
      </div>
      <footer class="card-footer">
        <div class="card-footer-item">
          <span>
            <slot />
          </span>
        </div>
      </footer>
    </div>
</template>

<script>
export default {
  name: 'Project',
  props: {
    name: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true
    },
    image: {
      type: String,
    },
    date: {
      type: String,
      required: true
    }
  }
}
</script>
<style scoped>
.image {
  display: flex;
  margin: auto;
  align-content: stretch;
}
.filter {
  filter: hue-rotate(170deg);
}
</style>