pipeline{
    agent {label 'webserver'}
    stages{
        stage(pull){
            steps{
                sh "pwd"
                sh "ls"
                sh "git pull https://github.com/Rohithhhhhhhhhh/my-sample-website.git"
            }
        }
        stage(build){
            steps{
                sh "ls"
                sh "mvn clean install"
            }
        }
        stage(deploy){
            steps{
                sh "cp /home/ec2-user/workspace/shellnew/my-sample-website/webapp/target/webapp.war /home/ec2-user/apache-tomcat-8.0.15/webapps"
            }
        }
    }
}
