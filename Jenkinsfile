@Library('newlibrary')_
node('built-in')
{
    stage('ContDownload_Master')
    {
        cicd.newGit("https://github.com/krishnain/maven16.git")
    }
    stage('ContBuild_Master')
    {
        cicd.newMaven()
    }
    stage('ContDeployment_Master')
    {
        cicd.newDeploy("ScriptedPipelinewithSharedlibraries","172.31.36.8","testapp")
    }
    stage('ContTesting_Master')
    {
        cicd.newGit("https://github.com/intelliqittrainings/FunctionalTesting.git")
                
        cicd.runSelenium("ScriptedPipelinewithSharedlibraries")
    }
    stage('ContDelivery_Master')
    {
        cicd.newDeploy("ScriptedPipelinewithSharedlibraries","172.31.45.149","prodapp")
    }
    
    
    
    
    
}
