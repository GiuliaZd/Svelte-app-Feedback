<script>
  import { fade, scale, slide } from "svelte/transition";
  import FeedbackItem from "./FeedbackItem.svelte";
  export let feedback = [];
</script>

{#each feedback as fb (fb.id)}
  <div in:fade={{ duration: 500 }} out:slide>
    <FeedbackItem item={fb} on:delete-feedback />
  </div>
{/each}
