<script lang="ts">
  import NavEle from '../lib/Components/NavEle.svelte';

	import '../app.postcss';
	import { AppShell, AppBar, LightSwitch } from '@skeletonlabs/skeleton';

	// Floating UI for Popups
	import { computePosition, autoUpdate, flip, shift, offset, arrow } from '@floating-ui/dom';
	import { storePopup } from '@skeletonlabs/skeleton';
	storePopup.set({ computePosition, autoUpdate, flip, shift, offset, arrow });
</script>
<head>
	<title>Simplistic Sounds</title>
</head>
<!-- App Shell -->
<AppShell>
	<svelte:fragment slot="header">
		<!-- App Bar -->
		<AppBar shadow="shadow-2xl" slotLead="hidden md:inline" >
			<svelte:fragment slot="lead">
				<strong class="text-xl uppercase hidden md:inline">Simplistic Sounds</strong>
			</svelte:fragment>
			<svelte:fragment slot="trail">
				<div class="flex justify-center gap-3 w-full">
				<NavEle name="Home" url="/"></NavEle>
				<NavEle name="Browse" url="/browse"></NavEle>
				<NavEle name="Community" url="/community"></NavEle>
				<NavEle name="Meet & Greet" url="/meetngreet"></NavEle>
			</div>
			<LightSwitch  />

			</svelte:fragment>
			
		</AppBar>
	</svelte:fragment>
	<!-- Page Route Content -->
	<slot />
</AppShell>
