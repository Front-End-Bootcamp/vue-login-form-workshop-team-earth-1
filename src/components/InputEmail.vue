<script setup>
	import { computed } from '@vue/reactivity';
	
			const props = defineProps(["name"])
			const emits = defineEmits(["update:name"])
	
			const nameHandler = (event) => {
					emits("update:name",event.target.value)
			}
			
			const emailValid = computed( () => {
					return (/^[a-zA-Z]+[a-zA-Z0-9_.]+@[a-zA-Z.]+[a-zA-Z]$/).test(props.name)
			})
	
	</script>
	
	
	<template>
					<input type="email" id="email" autocomplete="off" :value="props.name" @input="nameHandler" class="input" placeholder="E-mail" />
					<p v-if="!emailValid"> Geçersiz Email </p>
	</template>
	
	<style lang="scss" scoped>
	
					.input {
							width: 100%;
							border: 2px solid #6066ff;
							border-radius: 10px;
							padding: 0.4rem 1rem;
							font-size: 1.2rem;
							background-color: #fff;
							color: black;
							box-shadow: #18191A , 0px 50px 100px -20px, #18191A 0px 30px 60px -30px, #18191A 0px -2px 6px 0px inset;
	
							&:focus {
									outline: none;
							}
	
							&::placeholder {
									color: black;
									font-size: 15px;
							}
	
					}
			
	
	</style>