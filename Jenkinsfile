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

                
            
        
    }
}
