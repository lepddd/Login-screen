<script></script>

<span on:click={() => console.log('Redirect to forget password area')}>FORGET MY PASSWORD</span>

<style>
    span {
    position: relative;
    font-weight: 700;
    font-size: 12px;
    color: #00a8e8;
    cursor: pointer;
  }
  span:hover {
    color: #0092cc;
  }
  span::after {
    content: "";
    position: absolute;
    width: 145px;
    height: 1px;
    background-color: #00a8e8;
    bottom: 0;
    left: 0;
  }
  span:hover:after {
    background-color: #0092cc;
  }
</style>