<template>
  <section>
    <button @click="addNewSectionListItem">Add new section</button>
    <ul>
      <section-list-item v-for="(item, index) in sectionListItems" :key="index" :title="item.title" />
    </ul>
  </section>
</template>

<script>
import SectionListItem from './SectionListItem'
export default {
  name: 'section-list-container',

  components: {
    'section-list-item': SectionListItem
  },

  data () {
    return {
      sectionListItems: []
    }
  },

  methods: {
    addNewSectionListItem () {
      this.sectionListItems.push({ title: 'section demo' })
    }
  }
}
</script>
