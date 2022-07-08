<script>
  import { fade } from "svelte/transition";
  import ClickButton from "./ClickButton.svelte";
</script>

<div out:fade in:fade={{ delay: 500 }}>
  <p>Don’t have an account ?</p>
  <p>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit.Lorem ipsum dolor
    sit amet, consectetur adipiscing elit.
  </p>
  <ClickButton on:click title={"I WANT TO RESGISTER"} grey={true} />
</div>

<style>
  div {
    position: absolute;
    top: 50%;
    right: 70px;
    transform: translateY(-50%);
    width: 180px;
  }
  div p {
    margin-bottom: 20px;
    color: #2b2d42;
  }
  div p:first-child {
    font-weight: 700;
    font-size: 24px;
  }
  div p:last-child {
    font-weight: 400;
    font-size: 16px;
  }
</style>
