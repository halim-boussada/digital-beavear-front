<template>
  <section class="section">
    <b-message title="Info" color="primary" aria-close-label="Close message">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce id fermentum quam. Proin sagittis, nibh id
      hendrerit imperdiet, elit sapien laoreet elit
    </b-message>
    <div class="home_row">
      <card v-for=" project in projects" :name="project.name" class="child" :description="project.description"
        :image="project.image">
        Created on <a href="https://github.com/buefy/buefy">
          {{ project.date }}
        </a>
      </card>
      <cardButton class="child">
        <b-icon color="white" size="is-large" icon="plus"></b-icon>
      </cardButton>
    </div>
    <div class="my-4 px-2 center show__more">
      <b-button type="is-danger is-light">Show More</b-button>
    </div>
    <hr>
    <div class="home_row">
      <card v-for="theme in themes" :name="theme.name" class="child" :description="theme.description"
        :image="theme.image">
        Created on <a href="https://github.com/buefy/buefy">
          {{ theme.date }}
        </a>
      </card>
    </div>
    <div class="my-4 px-2 center show__more">
      <b-button type="is-danger is-light">Show More</b-button>
    </div>
  </section>
</template>

<script>
import Card from '~/components/Card'
import CardButton from '~/components/CardButton'

export default {
  name: 'IndexPage',
  layout: "authed",
  components: {
    Card,
    CardButton
  },
  data() {
    return {
      projects: [
        { name: "project 1", date: "22/04/2022" },
        { name: "Project 2", date: "22/04/2022" },
        { name: "Project 3", date: "22/04/2022" }
      ],
      themes: [
        { name: "Theme 1", date: "22/04/2022" },
        { name: "Theme 2", date: "22/04/2022" },
        { name: "Theme 3", date: "22/04/2022" },
        { name: "Theme 4", date: "22/04/2022" }
      ]
    }
  }
}
</script>
<style scoped>
.home_row {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;

}

.show__more {
  display: flex;
  flex-direction: row-reverse;
}

.child {
  width: 23%;
  height: 500px;
}
</style>
