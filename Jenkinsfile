pipeline{
    agent any
    stages{
    stage('Clon Repository'){
        /*Cloning the repository*/
        steps{
            checkout scm
        }

    }

    stage('Build Image'){
        steps{
            sh 'sudo docker build -t streamlit .'

        }
    }
    stage('Run Image'){
        steps{
            sh 'sudo docker run -d -p 8501:8501 --name aswin-streamlit streamlit'

        }
    }
    stage('Testing'){
        steps{
            echo 'process completed and deployed'
        }
    
    }
    }

    
    
    

}
