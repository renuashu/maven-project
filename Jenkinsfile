pipeline
{
    agent any
    stages{
        stage('scm checkout')
        {
            steps{
               git branch: 'master', url: 'https://github.com/renuashu/maven-project'
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
