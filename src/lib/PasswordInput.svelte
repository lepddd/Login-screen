<script>
  import Icon from "@iconify/svelte";
  import { createEventDispatcher } from "svelte";

  const dispatch = createEventDispatcher();

  export let title;
  export let currentArea;
  export let wrongPassword = false;

  let password;

  let inputType = "password";

  //Show text on input password
  function showPassword() {
    inputType = inputType === "password" ? "text" : "password";
  }

  //Dispatch event
  function handleInput() {
    dispatch("onInputChange", password.value);
  }
</script>

<p>{title}</p>
<div class="input-container">
  <input
    type={inputType}
    class:wrongPassword
    placeholder="Your password"
    bind:this={password}
    on:input={handleInput}
  />
  {#if currentArea === "SignIn"}
    <span style="cursor: initial;">
      <Icon class="icon" icon="bx:lock-open-alt" color="#8ba7c1" />
    </span>
  {:else if inputType === "password"}
    <span on:click={showPassword}>
      <Icon class="icon" icon="akar-icons:eye" color="#8ba7c1" />
    </span>
  {:else if inputType === "text"}
    <span on:click={showPassword}>
      <Icon class="icon" icon="akar-icons:eye-closed" color="#8ba7c1" />
    </span>
  {/if}
</div>

<style>
  p {
    font-weight: 700;
    font-size: 16px;
  }
  span {
    cursor: pointer;
  }
  .input-container {
    position: relative;
    margin-bottom: 20px;
    width: 100%;
    max-width: 280px;
  }
  .input-container :global(.icon) {
    width: 24px;
    height: 24px;
    position: absolute;
    right: 0;
    bottom: 50%;
    transform: translateY(50%);
  }
  .input-container input {
    width: 280px;
    height: 50px;
    border: none;
    border-bottom: 1px solid #8ba7c1;
    outline: none;
    font-weight: 700;
    font-size: 16px;
    padding-right: 30px;
  }
  .input-container input::placeholder {
    color: #8ba7c1;
  }
  .input-container input.wrongPassword {
    border-bottom: 1px solid #cf1b24;
  }
  .input-container input:focus {
    border-bottom: 1px solid #00a8e8;
  }
  .input-container input.wrongPassword:focus {
    border-bottom: 1px solid #cf1b24;
  }
</style>
