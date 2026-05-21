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
      cards: [
        { id: 1, title: 'Karte 1', description: 'Beschreibung 1' },
        { id: 2, title: 'Karte 2', description: 'Beschreibung 2' },
        { id: 3, title: 'Karte 3', description: 'Beschreibung 3' },
      ]
    }
  }
}
</script>