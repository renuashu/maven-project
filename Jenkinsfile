pipeline
{
    agent any
    stages{
        stage('scm checkout')
        {
            steps{
               git branch: 'main', url: 'https://github.com/renuashu/Maven-project-for-pipeline'
                }
        }
        stage('please compile code') 
        { 
            steps { withMaven(jdk: 'JDK_HOME', maven: 'MVN_HOME') 
                 {sh 'mvn compile'}
   
}

}

        }





    }
