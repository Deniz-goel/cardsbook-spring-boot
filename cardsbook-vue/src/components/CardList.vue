<template>
  <div class="card-list">
    <div v-for="card in cards" :key="card.id" class="card">
      <h3>{{ card.title }}</h3>
      <p>{{ card.description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CardList',
  data() {
    return {
      cards: []
    }
  },
  mounted() {
    fetch('https://DEIN-BACKEND.onrender.com/api/cards')
      .then(res => res.json())
      .then(data => this.cards = data)
  }
}
</script>