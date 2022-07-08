<script>
    import Icon from "@iconify/svelte";
</script>

<p>EMAIL</p>
<div class="input-container">
  <input type="text" placeholder="Your email adress" />
  <Icon class="icon" icon="ic:sharp-alternate-email" color="#8ba7c1" />
</div>

<style>
    p {
    font-weight: 700;
    font-size: 16px;
  }
  .input-container {
    position: relative;
    margin-bottom: 20px;
    width: 100%;
    max-width: 280px;
    background-color: #e5383b;
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
  .input-container input:focus {
    border-bottom: 1px solid #00a8e8;
  }
  .input-container input::placeholder {
    color: #8ba7c1;
  }
</style>
