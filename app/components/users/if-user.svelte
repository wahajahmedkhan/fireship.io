<svelte:options tag="if-user" />

<!-- Is signed in  -->

<script lang="ts">
  import { user } from '../../stores';
</script>

{#if $user}
    <slot></slot>
{:else}
    <slot name="signed-out"></slot>
{/if}
 