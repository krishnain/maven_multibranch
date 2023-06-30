@Library('mylibrary')_
node('built-in')
{
   stage('ContDownload_Master')
   {
       cicd.newGit("maven")    
   }
   stage('ContBuild_Master')
   {
       cicd.newMaven()
   }
   stage('ContDeployment_Master')
   {
      cicd.newDeploy("ScriptedPipelinewithSharedLibraries","172.31.7.30","mytestapp")
   }
   stage('ContTesting_Master')
   {
       cicd.newGit("FunctionalTesting")
       cicd.runSelenium("ScriptedPipelinewithSharedLibraries")
   }
   stage('ContDelivery_Master')
   {
      cicd.newDeploy("ScriptedPipelinewithSharedLibraries","172.31.7.247","myprodapp")
   }
   
   
}
