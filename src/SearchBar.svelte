<script>
    import { Input } from "@smui/textfield";
    import Paper from "@smui/paper";
    import Fab from "@smui/fab";
    import { Icon } from "@smui/common";

    let value = "";

    function doSearch() {
        alert("Search for " + value);
    }
</script>

<div class="solo-demo-container solo-container">
    <Paper class="solo-paper" elevation={6}>
        <Icon class="material-icons">search</Icon>
        <Input
            bind:value
            on:keydown={(event) => event.key === "Enter" && doSearch()}
            placeholder="Search"
            class="solo-input"
        />
    </Paper>
    <Fab
        on:click={doSearch}
        disabled={value === ""}
        color="primary"
        mini
        class="solo-fab"
    >
        <Icon class="material-icons">arrow_forward</Icon>
    </Fab>
</div>

<style>
    .solo-demo-container {
        padding: 36px 18px;
    }

    .solo-container {
        display: flex;
        justify-content: center;
        align-items: center;
    }
    * :global(.solo-paper) {
        display: flex;
        align-items: center;
        flex-grow: 1;
        max-width: 600px;
        margin: 0 12px;
        padding: 0 12px;
        height: 48px;
        background-color: #1c1c24;
    }
    * :global(.solo-paper > *) {
        display: inline-block;
        margin: 0 12px;
    }
    * :global(.solo-input) {
        flex-grow: 1;
        color: var(--mdc-theme-on-surface, #fff);
    }
    * :global(.solo-input::placeholder) {
        color: var(--mdc-theme-on-surface, #fff);
        opacity: 0.6;
    }
    * :global(.solo-fab) {
        flex-shrink: 0;
    }

    * :global(.material-icons){
        color: #fff;
    }
</style>
