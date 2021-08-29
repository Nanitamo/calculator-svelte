<script lang="ts">
  import Button from "./Button.svelte";
  import Line from "./Line.svelte";
  import Screen from "./Screen.svelte";
</script>

<div class="calculator">
  <Screen value="0" />
  <Line>
    <Button desta text="AC" tripple={true} />
    <Button op text="/" />
  </Line>

  <Line>
    <Button text="7" />
    <Button text="8" />
    <Button text="9" />
    <Button op text="*" />
  </Line>

  <Line>
    <Button text="4" />
    <Button text="5" />
    <Button text="6" />
    <Button op text="+" />
  </Line>

  <Line>
    <Button text="1" />
    <Button text="2" />
    <Button text="3" />
    <Button op text="-" />
  </Line>

  <Line>
    <Button dupple text="0" />
    <Button text="," />
    <Button desta text="=" />
  </Line>
</div>


<style>
  .calculator {
    background-color: var(--cor-fundo);
    height: 220px;
    width: 150px;
    padding: 10px;
    border-radius: 10px;

    display: flex;
    flex-direction: column;
  }

</style>
