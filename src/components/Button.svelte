<script lang="ts">
    import { createEventDispatcher } from "svelte";

    export let text = "";
    export let isSecondary = true;
    const dispatch = createEventDispatcher();

    function handleClick() {
        dispatch("click");
    }
</script>

<button
    class="button"
    class:button--secondary={isSecondary}
    on:click={handleClick}>{text}</button
>

<style lang="scss">
    .button {
        display: inline-flex;
        justify-content: center;
        align-items: center;
        padding: 18.5px 42px;
        transition: 0.3s;
        border: none;
        border-radius: 4px;
        cursor: pointer;

        color: var(--clr-primary-alt);
        background-color: var(--clr-accent);

        &:hover {
            background-color: var(--clr-accent-active);
        }

        &.button--secondary {
            color: var(--clr-primary-alt);
            background-color: var(--clr-secondary-alt);

            &:hover {
                background-color: var(--clr-secondary-alt-active);
            }
        }
    }
</style>
