<template>
  <div class="main-content">
  <Nav-module/>
  <Main-module/>
</div>
</template>

<style>
  body {
    background-color: rgb(17, 17, 17);
    color: #fff;
  }

  .footer {
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 5rem;
    background-color: #242323;
    padding: 3rem;
    text-align: center;
  }
</style>

<script>
export default {
  name: 'IndexPage',
  mode: 'server'
}
</script>
