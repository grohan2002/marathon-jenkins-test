node{

    stage ('Clone Source')
    {
        echo "#>Cloning Sources."
        checkout scm
    }

    stage ('Marathon Deploy')
    {
        echo "#>Deploying to marathon"
        marathon(            
            credentialsId: 'dcos-auth-token',
            docker: '', 
            env: [[name: 'JOB_NAME', value: 'test-pipelin']], 
            id: '/hello-world-test', 
            url: 'http://mesos-test.nexla.com/service/marathon'
        )
    }

}