<template>
  <div class="person">
    <div>
      <img :src="getImg" />
    </div>
    <h2>{{ person.name }}</h2>
    <p>
      <em>{{ person.info }}</em>
      {{ person.age }} years old!
    </p>
    <footer>
      <small>{{ person.number }}</small>
      <router-link :to="{ path: `/person/${person.id}` }" class="button">View</router-link>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'Person',
  props: {
    person: {
      type: Object,
      required: true
    },
    img: {
      type: Number,
      required: true,
    }
  },
  data() {
    return {}
  },
  computed: {
    getImg() {
      return `https://randomuser.me/api/portraits/men/${this.img}.jpg`
    }
  }
}
</script>

<style lang='scss' scoped>
.person {
  background-color: rgb(151, 146, 146);
  border-radius: 20px;
  padding: 20px;

  footer {
    display: flex;
    justify-content: space-between;

    .button {
      padding: 5px 10px;
      border: none;
    }
  }
}
</style>