<script setup>
import { ref } from 'vue'

defineProps({
  title: {
    type: String,
    required: true
  }
})

const data = ref([
	{
		id: 1,
		name: 'krisna'
	},
	{
		id: 2,
		name: 'firdaus'
	}
])

</script>

<template>
	<div>
		{{ title }}
	</div>
	<div>
		<ul>
			<li v-for="item in data" :key="item.id">
				{{ item.id }} / {{ item.name }}
			</li>
		</ul>
	</div>
</template>

<style>
</style>