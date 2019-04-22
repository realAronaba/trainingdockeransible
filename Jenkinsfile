node {
   stage('Check The sources files')
   {
      checkout scm
      }
   stage('Running the playbooks')
    {
        ansiblePlaybook(
            playbook: 'webserver.yml',
            inventory: 'inventory.ini',
            credentialsId: 'ansible_jenkins')
         }
   stage('Delete workspace')
        {
           deleteDir()
        }
}
