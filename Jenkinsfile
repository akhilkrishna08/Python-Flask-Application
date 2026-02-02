pipeline 
{
    agent any

    stages 
    {
        stage('clone')
        {
            steps 
            {
                git 'https://github.com/akhilkrishna08/Python-Flask-Application.git'
            }
        }
        
        stage('Build Docker Image') 
        {
            steps 
            {
                script 
                {
                    sh 'docker build -t my-flask-app:latest .'
                }
            }
        }
        stage('Run Container') 
        {
            steps 
            {
                script 
                {
                     sh 'docker stop flask-container || true'
                     sh 'docker rm flask-container || true'
                     sh 'docker run -d -p 5000:5000 --name flask-container flask-devops-app:latest'
                }
            }
        }
   }
}

                
            

