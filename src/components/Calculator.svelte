<script lang="ts">
  import Button from "./Button.svelte";
  import Line from "./Line.svelte";
  import Screen from "./Screen.svelte";

  let value = '0'

  class Model {
    value: string

    constructor(value: string = '0'){
      this.value = value
    }
  }

  let obj = new Model()
  
  
  function digitedNumber(number: string) {
    obj.value += number 
  }
</script>

<div class="calculator">
  <Screen value={obj.value} />
  <Line>
    <Button desta text="AC" tripple={true} />
    <Button op text="/" />
  </Line>

  <Line>
    <Button text="7" onClick={digitedNumber} />
    <Button text="8" onClick={digitedNumber} />
    <Button text="9" onClick={digitedNumber} />
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
