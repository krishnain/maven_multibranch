@Library('mylibrary')_
node('built-in')
{
   stage('ContDownload_Loans')
   {
       cicd.newGit("maven")    
   }
   stage('ContBuild_Loans')
   {
       cicd.newMaven()
   }
   
   
}
