pipeline 
{
   agent any

   tools {
       maven 'maven'
       jdk 'Java'
         }
  environment 
  {
     dockerhub=credentials('dockerhub')
  }
   stages
   {
       stage("clean")
       {
         when{
                branch "scala"
                }
      
         steps
            {
                sh 'mvn clean'
            }
       }
      
       stage("test"){
          when{
                branch "scala"
                }
      
         steps
            {
                sh 'mvn test'
            }
       }
      }
     }
       
