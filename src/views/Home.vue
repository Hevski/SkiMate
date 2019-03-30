<template lang="html">
  <div class="">
    <h1>SkiMate</h1>
    <section v-if="skis">
			<ski-summary-home v-for="(ski, index) in skis" :key="index" :ski="ski"></ski-summary-home>
		</section>
  </div>
</template>

<script>
import SkiSummaryHome from '../components/SkiSummaryHome.vue';
export default {
  name: "Home",
  components: {
    SkiSummaryHome
  },
  data() {
  return {
    skis: []
  }
},
mounted(){
		fetch("http://localhost:3000/api/skiInfo/")
		.then(res => res.json())
		.then(data => this.skis = data)
	},
}
</script>

<style lang="css" scoped>
</style>
