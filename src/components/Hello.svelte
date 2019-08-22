<script>
    import { onMount } from 'svelte';
    import { fly, fade } from 'svelte/transition';

    let visible = true;
    const bye = () => visible = false;

</script>

{#if visible}
    <div transition:fly="{{x: -30, duration: 700}}" on:click={bye}>
        <span>Hello,</span>
        <span>I'm</span>
        <span>Diogo.</span>
    </div>
{/if}

<style>
    div {
        display: flex;
        flex-direction: column;
        background-color: purple;
        position: absolute;
        padding: 10px;
        line-height: 1.35;
        top: 50%;
        left: 10%;
        transform: translateY(-50%);
        color: white;
        font-family: 'Courier New', Courier, monospace;
        font-size: 32px;
    }
</style>
