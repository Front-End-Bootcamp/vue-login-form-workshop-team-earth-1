<script setup>
import RegisterComp from './components/Auth/RegisterComp.vue';

</script>

<template>
	<RegisterComp />
</template>

<style >
:root {
	--primary: #6066ff;
	--secondary: #8b54ff;
	--placeholder: #4d4d4d;
	--white: #ffffff;
}

/* Global */
.flex {
	display: flex;
}

.flex-column {
	flex-direction: column;
}

.items-center {
	align-items: center;
}

::placeholder {
	color: var(--placeholder)
}

button,
.button__primary {
	cursor: pointer;
	width: 100%;
	border: 0;
	border-radius: 25px;
	background-color: var(--primary);
	color: var(--white);
	padding: 8px 0;
}

.button__secondary {
	background-color: var(--secondary);
	color: var(--white);
}

/* Auth */

.auth {
	width: 300px;
	padding: 0 25px;
	border-radius: 15px;
	gap: 15px;
}

.auth--title {
	color: var(--primary);
	font-weight: 700;
	font-size: 35px;
	margin-bottom: 40px;
}

.auth--button {
	width: 100%;
	margin-top: 40px;
	display: flex;
	flex-direction: column;
	gap: 15px;
}

/* Register */
.register input {
	width: 100%;
	border: 2px solid var(--primary);
	border-radius: 8px;
	padding: 6px 8px;
	outline: 0;

}

/* Login */
.login input {
	width: 100%;
	border: 2px solid var(--primary);
	border-radius: 25px;
	padding: 6px 8px;
	outline: 0;
}
</style>

