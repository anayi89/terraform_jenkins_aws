String credentialsId = 'awsCredentials'
stage('Initialize') {
    node {
        withCredentials([[
            $class: 'AmazonWebServicesCredentialsBinding',
            credentialsId: credentialsId,
            accessKeyVariable: 'AWS_ACCESS_KEY_ID',
            secretKeyVariable: 'AWS_SECRET_ACCESS_KEY'
        ]]) {sh 'cd /home/centos/devops_project1 | /usr/local/bin/terraform init'}
    }
}
stage('Plan') {
    node {
        withCredentials([[
            $class: 'AmazonWebServicesCredentialsBinding',
            credentialsId: credentialsId,
            accessKeyVariable: 'AWS_ACCESS_KEY_ID',
            secretKeyVariable: 'AWS_SECRET_ACCESS_KEY'
        ]]) {sh 'cd /home/centos/devops_project1 | /usr/local/bin/terraform plan'}
    }
}
stage('Apply') {
    node {
        withCredentials([[
            $class: 'AmazonWebServicesCredentialsBinding',
            credentialsId: credentialsId,
            accessKeyVariable: 'AWS_ACCESS_KEY_ID',
            secretKeyVariable: 'AWS_SECRET_ACCESS_KEY'
        ]]) {sh 'cd /home/centos/devops_project1 | /usr/local/bin/terraform apply'}
    }
}
stage('Show') {
    node {
        withCredentials([[
            $class: 'AmazonWebServicesCredentialsBinding',
            credentialsId: credentialsId,
            accessKeyVariable: 'AWS_ACCESS_KEY_ID',
            secretKeyVariable: 'AWS_SECRET_ACCESS_KEY'
        ]]) {sh 'cd /home/centos/devops_project1 | /usr/local/bin/terraform show'}
    }
}
