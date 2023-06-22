<template>
    <div>
        <Nav-module/>
        <h1 class="margin-custom h1 text-bold d-none d-md-block">Meus Projetos</h1>
        <Cards-module/>
        <Footer-module class="Footer-module"/>
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
    margin-top: 12rem;
    background-color: #242323;
    padding: 3rem;
    text-align: center;
  }

  .margin-custom {
    margin-top: 5rem;
    margin-left: 8rem;
  }
</style>