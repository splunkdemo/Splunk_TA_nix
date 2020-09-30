pipeline {

    agent any
   //   stage('Git checkout') {
        //  Get some code from a GitHub repository
       // git 'https://github.com/gvamsius/simplexml.git'
     //            }
    stages{

		stage('send artifacts to ansible server') {
		   //sshPublisher(publishers: [sshPublisherDesc(configName: 'ansible-master', transfers: [sshTransfer(cleanRemote: false, excludes: '', execCommand: '', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: '//opt//ansible//splunkdemo', remoteDirectorySDF: false, removePrefix: '', sourceFiles: '**/*')], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)])
		   // sshPublisher(publishers: [sshPublisherDesc(configName: 'ansible-master', transfers: [sshTransfer(cleanRemote: false, excludes: '', execCommand: 'cd /opt/ansible/playbooks; ansible-playbook -i splunkhosts splunk_deploy.yml', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: '//opt//ansible//splunkdemo', remoteDirectorySDF: false, removePrefix: '', sourceFiles: '**/*')], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)])
		
			steps{
			
			sshPublisher(publishers: [sshPublisherDesc(configName: 'ansible-master', transfers: [sshTransfer(cleanRemote: false, excludes: 'Jenkinsfile', execCommand: 'cd /opt/ansible/playbooks/deploymentapps; ansible-playbook -i splunkhosts splunk_deploymentserver.yml -vv', flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: '//opt//ansible//splunkdeploymentapps', remoteDirectorySDF: false, removePrefix: '', sourceFiles: '**/*')], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)])
				}

			} 
		}    
  
    
	}
