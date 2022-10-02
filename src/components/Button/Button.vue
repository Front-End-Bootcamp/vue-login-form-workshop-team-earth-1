<script setup>

	const props = defineProps(["name","type","click","isActive"])

</script>


<template>
	<div>
		<button type="button" class="button" :class="props.type" @click="props?.click" :disabled="props?.isActive" > {{props.name}} </button>
	</div>
</template>


<style lang="scss" scoped>
	
	.button{
		width: 100%;
		padding: 10px 10px;
		border: none;
		border-radius: 20px;
		font-size: 14px;
		background-color: #8b54ff;
		color: #fff;
		margin-top: 12px;
		cursor: pointer;
		transition: all 0.3s ease-in-out;

		&:disabled{
			cursor: not-allowed;
		}

	}

	.register{
		background-color: #8b54ff;
	}

	.signIn {
		background-color: #6066ff;
	}

	.login{
		width: 40%;
		background-color: #252eff;
	}
		
	
	


</style>