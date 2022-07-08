<script>
  export let title;
  export let btnType = 'button';

  export let red = false, grey = false;

</script>

<input type={btnType} value={title} class:red class:grey on:click|preventDefault>

<!-- <button class:red class:grey on:click>{title}</button> -->

<style>
  .red {
    cursor: pointer;
    width: 100px;
    height: 50px;
    background: #e5383b;
    box-shadow: 0px 3px 7px -3px rgba(0, 0, 0, 0.3),
      0px 6px 12px -2px rgba(50, 50, 93, 0.25);
    border-radius: 2px;
    border: none;
    color: white;
    font-size: 14px;
    font-weight: 700;
  }
  .red:hover {
    background: #cf1b24;
    transition: 0.2s ease-in-out;
  }
  .grey {
    background: #8ba7c1;
    box-shadow: 0px 10px 10px -5px rgba(0, 0, 0, 0.04),
      0px 20px 25px -5px rgba(0, 0, 0, 0.1);
    border-radius: 2px;
    width: 180px;
    height: 50px;
    border: none;
    color: #fff;
    font-weight: 700;
    font-size: 14px;
    cursor: pointer;
  }
  .grey:hover {
    background-color: #7495b4;
    transition: 0.2s ease-in-out;
  }
</style>
