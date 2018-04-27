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
            credentialsId: '512a204c-8ebc-428c-8b9b-49701b155b33', 
            docker: '', 
            env: [[name: 'JOB_NAME', value: 'test-pipelin']], 
            id: '', 
            url: 'http://mesos-test.nexla.com'
        )
    }

}