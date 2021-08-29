<script lang="ts">
    export let text: string
    export let tripple: boolean = false
    export let dupple: boolean = false
    export let op: boolean = false
    export let desta: boolean = false
    export let onClick: (valor:string) => void = () =>{}

    function click() {
        
    }
</script>

<button class= 'botao' 
        on:click={() =>onClick(text)}
        class:tripple class:dupple class:op class:desta >
        {text}
</button>

<style>
    .botao{
        margin: 0%;
        border: 1px solid var(--cor-fundo);
        flex-basis: 25%;
    }

    .tripple{
        flex-basis: 75%;
    }

    .dupple{
        flex-basis: 50%;
    }
    .op{
        background-color: orange;
        color: white;
    }
    .desta{
        background-color: red;
        color: white;
    }

</style>