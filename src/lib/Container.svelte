<script>
  import SignInArea from "./SignInArea.svelte";
  import SignInBanner from "./SignInBanner.svelte";
  import SignUpArea from "./SignUpArea.svelte";
  import SignUpBanner from "./SignUpBanner.svelte";

  /* let options = ['SignUp','SignIn'] */

  let currentArea = 'SignIn';

  /* $:console.log(currentArea) */

</script>

<div class="container">
  {#if currentArea == 'SignIn'}
    <SignInArea  {currentArea}/>
    <SignUpBanner on:click={() => (currentArea = 'SignUp')} />
  {:else}
    <SignUpArea {currentArea}/>
    <SignInBanner on:click={() => (currentArea = 'SignIn')} />
  {/if}
</div>

<style>
  .container {
    position: relative;
    width: 800px;
    height: 450px;
    box-shadow: 0px 10px 10px -5px rgba(0, 0, 0, 0.04),
      0px 20px 25px -5px rgba(0, 0, 0, 0.1);
    border-radius: 5px;
    background-color: #edf6f9;
  }
</style>
