pipeline{
    agent any{

        stages{
            stage('Clonar o repositório'){
                steps{
                    git branch: 'main', url: 'https://github.com/FelipeSilvaPortifolio/teste-api-ebac.git'
                }

            stage('Instalar dependencias'){
                steps{
                    sh 'npm install'
                }
            }

            stage('Executar testes'){
                steps{
                    sh 'NO_COLOR=1 npm run cy:run'
                }
            }
        }
    }
}