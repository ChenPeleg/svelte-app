<script lang="ts">
const data: string = '.<br> This is an aditional Data';
const click_button = (event: Event) => {
  alert('clicked');
};
</script>

<main class="help-component">
  this is my help component {@html data}

  <br />
  <button on:click="{click_button}">Click me!</button>
</main>

<style>
main.help-component {
  font-size: large;
  border-radius: 15px;
  padding: 1em;
  margin: 1em;
  width: 200px;
  min-height: 150px;
  background-color: rgb(16, 8, 32);
}
</style>
