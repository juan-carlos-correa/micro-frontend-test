<template>
  <section>
    <h2>ADD SECTION</h2>
    <div>Add section</div>
    <div v-for="section in sections" :key="section.id">
      {{ section.name }}
    </div>
  </section>
</template>

<script>
export default {
  data () {
    return {
      sections: []
    }
  }
}
</script>
