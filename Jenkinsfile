pipeline {
    agent any


    stages {
        stage('Clonar o repositório') {
            steps {
                git branch: 'main', url: 'https://github.com/beatrism/testes-api-rest.git'
            }
        }

    
        stage('Instalar dependencias') {
             
            steps {
                nodejs('node'){
                    bat 'npm install'
                            }
                    }
        }

        stage('Subir servidor e Executar Testes') {
            steps {
                 nodejs('node'){
                    bat 'npx serverest'
                }
                        }
            steps {
                 nodejs('node'){
                    bat 'npx cypress run'
                }
                        }
        }
    

}
    
    
}
