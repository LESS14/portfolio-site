<template>
    <footer class="footer">
      <p>Portfólio - Felipe Maciel | <a href="https://www.github.com/LESS14/portfolio-site" target="_blank">Veja o código fonte desse site no Github</a></p>
    </footer>
  </template>
  
  <script>
  export default {
    computed: {
      deployDate() {
        return process.env.DEPLOY_DATE || '';
      },
    },
  };
  </script>
  