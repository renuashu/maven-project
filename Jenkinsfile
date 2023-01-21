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
             stage('please test code') 
        { 
            steps { withMaven(jdk: 'JDK_HOME', maven: 'MVN_HOME') 
                 {sh 'mvn test'}

}
             stage('please build code') 
        { 
            steps { withMaven(jdk: 'JDK_HOME', maven: 'MVN_HOME') 
                 {sh 'mvn package'}
                  }

}

        }





    }
