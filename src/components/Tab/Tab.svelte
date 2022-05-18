<script setup lang="ts">
    import Button from "../Button/Button.svelte";

    export let tab: { 
        buttonText: string;
        paneText: string;
    }[];

    let currentTab = 0;
    
    const onSelect = (tabIndex: number) => {
        currentTab = tabIndex;
    };
</script>

<div class="tab">
    <div class="buttons">
        {#each tab as tabItem, index (tabItem)}
        <Button
            text={tabItem.buttonText}
            selected={currentTab === index}
            index={index}
            on:selection={e => onSelect(e.detail)}
        />
    {/each}
    </div>

    <div class="pane">{tab[currentTab].paneText} </div>
</div>


<style>
    .buttons {
		display: flex;
	}
    .pane {
		padding: 20px;
		margin: 10px 0;
		width: 800px;
		border-radius: 10px;
		border: 1px solid #aaa;
		background-color: #f0f0f0;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 24px;
	}
    .tab {
        display: flex;
        flex-direction: column;
        align-items: center;
    }
</style>