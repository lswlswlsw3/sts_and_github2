def workspace;

node {
	stage('check out')
	{
		checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'a9c37976-2e26-4661-934e-ad5055bf687d', url: 'https://github.com/lswlswlsw3/sts_and_github2.git']]])
		workspace = pwd()
	}
	stage('Static Code Analysis')
	{
		echo "Static code Analysis!!"
	}
	stage('Build')
	{
		
		sh "./gradlew clean build"
	}
	stage('Unit Testing')
	{
		echo "Unit Testing!!"
	}
	stage('Delivery')
	{
		echo "Delivery!!"
	}
}