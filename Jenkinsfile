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

}
         stage('please build code') 
        { 
            steps { withMaven(jdk: 'JDK_HOME', maven: 'MVN_HOME') 
                 {sh 'mvn package'}
                  }

}
            

        

stage('deploy to tomcat')
{
steps
{
sshagent(['167fc2b5-1c7d-4518-a866-e324d3248d7e']) {
    sh 'scp -o StrictHostKeyChecking=no */target/webapp.war ec2-user@172.31.90.137:/var/lib/tomcat/webapps/'
}
}
}
    }
}





    
