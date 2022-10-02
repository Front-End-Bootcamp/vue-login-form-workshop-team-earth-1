<script setup>
const emits = defineEmits(["update:password", "isValid"]);

const inputHandler = (e) => {
	const isValid =
		/^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)(?=.*[@$!%*?&])[A-Za-z\d@$!%*?&]{8,}$/.test(
			e.target.value
		);

	if (isValid) {
		emits("update:password", e.target.value);
		return;
	}

	emits("isValid", false);
	return;
};

const props = defineProps(["type", "password"]);
</script>

<template>
	<div>
		<input
			:type="type"
			id="passwordInput"
			:value="props.password"
			@input="inputHandler"
		/>
	</div>
</template>
