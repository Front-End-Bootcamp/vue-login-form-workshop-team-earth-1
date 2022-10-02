<script setup>
	const emits = defineEmits(["update: phoneNumber", "isValid"]);
	
	const inputHandler = (e) => {
		const isValid =
			/^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)(?=.*[@$!%*?&])[A-Za-z\d@$!%*?&]{8,}$/.test(
				e.target.value
			);
	
		if (isValid) {
			emits("update: phoneNumber", e.target.value);
			return;phoneNumber
		}
	
		emits("isValid", false);
		return;
	};
	
	const props = defineProps(["phoneNumber"]);
	</script>
	
	<template>
		<div>
			<input
				:type="type"
				id="phoneNumber"
				:value="props.phone"
				@input="inputHandler"
			/>
		</div>
	</template>