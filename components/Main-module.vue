<template>
    <div class="content">
        <h1 class="h1 text-bold title">Olá, seja bem-vindo ao meu site pessoal!</h1>
        <p>Me chamo Felipe Maciel e sou arquiteto de software e desenvolvedor de software.</p>

        <div class="projects__section">
            <h3 class="text-bold mt-5">Veja alguns dos meus projetos individuais</h3>
            <Cards-module/>
        </div>

        <div class="links__section">
            <h3 class="text-bold mt-5">Links de redes sociais</h3>
            <b-button variant="outline-primary" href="https://felipe.ebxdesignstudio.com/links" target="_blank">Acesse meu agregador de links</b-button>
        </div>

        <Footer-module/>
    </div>
</template>

<style>
    .title::before {
        content: "\1F44B";
    }

    .content {
        text-align: center;
        margin-top: 5rem;
    }
</style>