node('built-in') 
{
    stage('Continuous Download') 
	{
    git 'https://github.com/sunildevops77/maven.git'
	}
    stage('Continuous Build') 
	{
    sh 'mvn package'
	}
    stage('Continuous Deployment') 
	{
 'scp /home/ubuntu/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war   ubuntu@172.31.26.217:/var/lib/tomcat9/webapps/qaenv.war'
	}
    stage('Continuous Testing') 
	{
              sh  'echo "Testing Passed'
	}
    stage('Continuous Delivery') 
	{
 'scp /home/ubuntu/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war   ubuntu@172.31.22.88:/var/lib/tomcat9/webapps/prodenv.war'
	}
}
