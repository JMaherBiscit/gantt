<script>
	import { createEventDispatcher } from "svelte";
	const dispatch = createEventDispatcher();

	export let appearance = "primary";
	export let icon = "";

</script>

<button class="wx-button {appearance}" on:click={() => dispatch('click')}>
	{#if icon}<i class="wx-button-icon {icon}" />{/if}
</button>

<style>
	.wx-button {
		width: 50px;
		height: 50px;
		border: none;
		outline: none;
		border-radius: 50%;
		cursor: pointer;
	}

	.wx-primary {
		color: var(--wx-color-primary-font);
		background-color: var(--wx-color-primary);
	}

	.wx-primary:hover {
		background-color: #0b9db1;
	}

	.wx-transparent {
		width: 40px;
		height: 40px;

		color: var(--wx-color-primary-font);
		background-color: rgba(99, 99, 99, 0.45);
	}

	.wx-transparent:hover {
		background-color: rgba(69, 69, 69, 0.45);
	}

	.wx-button-icon {
		font-size: 20px;
	}

</style>
