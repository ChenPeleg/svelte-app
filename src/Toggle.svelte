<script type="ts">
import { mode } from './store';

const isLightModeOn = $mode === 'light';
const isDarkModeOn = $mode === 'dark';
const isAutoModeOn = $mode === 'auto';

function handleClick(e: Event): void {
  const { value } = e.target as HTMLInputElement;
  mode.update(() => value);
}
</script>

<div>
  <label on:click="{handleClick}">
    <input
      type="radio"
      id="light"
      name="mode"
      value="light"
      checked="{isLightModeOn}"
    />
    Light mode
  </label>

  <label on:click="{handleClick}">
    <input
      type="radio"
      id="dark"
      name="mode"
      value="dark"
      checked="{isDarkModeOn}"
    />
    Dark mode
  </label>

  <label on:click="{handleClick}">
    <input
      type="radio"
      id="auto"
      name="mode"
      value="auto"
      checked="{isAutoModeOn}"
    />
    Auto
  </label>
</div>
