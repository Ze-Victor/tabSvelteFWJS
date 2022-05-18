<script setup lang="ts">
    import { createEventDispatcher } from "svelte";

    export let text: string;
    export let selected: boolean;
    export let index: number;

    const dispatcher = createEventDispatcher();

    export const onClick = (index: number) => {
        dispatcher('selection', index);
    };
    
</script>

<div class="buttons">
    <button
      class={ selected ? 'selected' : '' }
      on:click={ e => onClick(index) } >
      { text }
    </button>
</div>

<style>
  button {
    margin-right: 10px;
    background-color: #ccc;
    border: 1px solid rgb(118, 118, 118);
    border-radius: 3px;
    padding: 4px 10px;
    font-size: 18px;
  }
  .selected {
    font-weight: bold;
    background-color: #aaa;
  }
  .buttons {
    margin-bottom: 10px;
  }
</style>