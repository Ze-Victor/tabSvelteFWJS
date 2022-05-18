<script lang="ts">
	import Tab from "./components/Tab/Tab.svelte";


	const tab =  [
      {
        "buttonText": "Tab 1",
        "paneText": "Texto 1",
      },
      {
        "buttonText": "Tab 2",
        "paneText": "Texto 2",
      },
      {
        "buttonText": "Tab 3",
        "paneText": "Texto 3",
      },
      {
        "buttonText": "Tab 4",
        "paneText": "Texto 4",
      },
    ];

</script>

<main>
	<Tab tab={tab}/>
</main>

<style>
	main {
		width: 100%;
		height: 100vh;

		display: flex;
		justify-content: center;
		align-items: center;
	}
</style>