//para executar essa pipeline é necessários estar com o servidor Serverest rodando na porta 3000
pipeline {
    agent any

    stages {
        stage('Clonar o repositorio') {
            steps {
                git branch: 'main', url: 'https://github.com/QA-ThalitaOyara/testes-e2e-ebac-shop.git'
            }
        }
    stage('Instalar dependencias') {
            steps {
            bat 'npm install'   
            }
        }
    stage('Executar testes') {
            steps {
            bat 'npm run cy:run'    
            }
        }
    }
}
