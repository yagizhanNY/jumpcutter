<!--
Copyright (C) 2020, 2021, 2022  WofWca <wofwca@protonmail.com>

This file is part of Jump Cutter Browser Extension.

Jump Cutter Browser Extension is free software: you can redistribute it and/or modify
it under the terms of the GNU Affero General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

Jump Cutter Browser Extension is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU Affero General Public License for more details.

You should have received a copy of the GNU Affero General Public License
along with Jump Cutter Browser Extension.  If not, see <https://www.gnu.org/licenses/>.
-->

<svelte:options
  immutable={true}
/>
<script lang="ts">
  export let label: string;
  export let checked: boolean;
</script>

<!-- Wrapper div so consecutive checkboxes are displayed on top of each other. -->
<div style="margin: 0.75rem 0;">
  <label>
    <input
      type="checkbox"
      {...$$restProps}
      bind:checked
    > {label}
  </label>
</div>

<style>
  input {
    /* So emojis aren't so close to the checkbox so they don't look too confusing together */
    margin-right: 0.4rem;
  }
</style>
