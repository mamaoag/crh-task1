<template>
    <div id="section-header">
        <h1><span class="square">&nbsp;</span> <slot /></h1>
        <hr id="section-border">
    </div>
</template>

<style>
    #section-border {
        margin-top: -6px;
        border: 3px solid var(--color-primary);
    }

    .square {
        width: 4.95px;
        background: linear-gradient(var(--color-primary), var(--color-secondary));
        margin-right: 10px;
    }

    .square, #section-header > h1 {
        vertical-align: middle;
    }
    
    #section-header > h1 {
        text-shadow: 0 1px rgba(0,0,0, 0.75);
        font-weight: 400;
        font-size: 28px;
        text-transform: uppercase;
    }
</style>