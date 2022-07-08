<script>
  import { fly, fade } from "svelte/transition";
  import PasswordInput from "./PasswordInput.svelte";
  import EmailInput from "./EmailInput.svelte";
  import ClickButton from "./ClickButton.svelte";
  import ForgetPassword from "./ForgetPassword.svelte";

  export let currentArea
</script>

<div class="login" out:fade in:fly={{ x: -400, duration: 1000 }}>
  <div class="content">
    <EmailInput />
    <PasswordInput title="PASSWORD" {currentArea}/>
    <div class="lower-container">
      <ForgetPassword />
      <ClickButton title={"LOGIN"} red={true}/>
    </div>
  </div>
</div>

<style>
  .login {
    display: flex;
    align-items: center;
    justify-content: center;
    position: absolute;
    top: 0;
    left: 0;
    width: 480px;
    height: 450px;
    box-shadow: 5px 0 5px -2px rgba(0, 0, 0, 0.2);
    border-radius: 5px 0px 0px 5px;
    background-color: #fff;
  }
  .lower-container {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 280px;
  }
</style>
