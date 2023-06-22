<template>
    <div class="container">
      <b-card-group class="card-group-spacing">
        <b-card v-for="project in projects" :key="project.id" :title="project.name" :img-src="project.image" img-alt="" class="bg-dark text-white card-3d mr-3 mt-md-3 mt-5">
          <p class="card-text">{{ project.description }}</p>
          <b-link :href="project.githubLink" target="_blank" class="github-link">
            <span class="github-text">Ver no GitHub</span>
            <arrow-right-icon/>
          </b-link>
        </b-card>
      </b-card-group>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        projects: [
          {
            id: 1,
            name: 'Tasker',
            description: 'Um simples gerenciador de tarefas totalmente escrito em Python',
            image: '',
            githubLink: 'https://github.com/LESS14/tasker'
          },
          {
            id: 2,
            name: 'QR Code Generator',
            description: 'Um simples gerador de QR Code escrito em C# e Javascript',
            image: '',
            githubLink: 'https://github.com/LESS14/QR-code-generator'
          },
          {
            id: 3,
            name: 'Color Picker',
            description: 'Um Color Picker totalmente escrito em C++',
            image: '',
            githubLink: 'https://github.com/LESS14/Color-Picker'
          },
          
        ]
      };
    }
  };
  </script>
  
  <style scoped>
  .github-link {
    position: relative;
    display: inline-block;
    color: inherit;
    text-decoration: none;
    transition: color 0.3s;
  }
  
  .github-link:hover {
    color: #007bff;
  }
  
  arrow-right-icon {
    display: inline-block;
    margin-left: 5px;
    transition: transform 0.3s;
  }
  
  .github-link:hover arrow-right-icon:hover {
    transform: translateX(-5px);
  }
  
  .github-text {
    position: relative;
  }
  
  .github-text:before {
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    width: 0;
    height: 2px;
    background-color: #007bff;
    transition: width 0.3s;
  }
  
  .github-link:hover .github-text:before {
    width: 100%;
  }

  .card-3d {
  transition: transform 0.5s;
}

.card-3d:hover {
  transform: perspective(1000px) rotateY(-10deg);
}

.card-group-spacing {
  margin-bottom: 20px;
}

@media (max-width: 767px) {
  .mobile-title {
    /* Estilos específicos para dispositivos móveis */
    margin-top: 0;
    /* Outras propriedades de estilo para dispositivos móveis */
  }
}
  </style>
  