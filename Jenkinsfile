String credentialsId = 'awsCredentials'
stage('Set Path') {
    node {
        withEnv(['terraform=/usr/local/bin/terraform'])
        withCredentials([[
            $class: 'AmazonWebServicesCredentialsBinding',
            credentialsId: credentialsId,
            accessKeyVariable: 'AWS_ACCESS_KEY_ID',
            secretKeyVariable: 'AWS_SECRET_ACCESS_KEY'
        ]]) {sh 'terraform init'}
        {sh 'terraform plan'}
        {sh 'terraform apply'}
        {sh 'terraform show'}
    }
}
stage('Initialize') {
    node {
    }
}
stage('Plan') {
    node {
        withCredentials([[
            $class: 'AmazonWebServicesCredentialsBinding',
            credentialsId: credentialsId,
            accessKeyVariable: 'AWS_ACCESS_KEY_ID',
            secretKeyVariable: 'AWS_SECRET_ACCESS_KEY'
        ]]) {sh 'terraform plan'}
    }
}
stage('Apply') {
    node {
        withCredentials([[
            $class: 'AmazonWebServicesCredentialsBinding',
            credentialsId: credentialsId,
            accessKeyVariable: 'AWS_ACCESS_KEY_ID',
            secretKeyVariable: 'AWS_SECRET_ACCESS_KEY'
        ]]) {sh 'terraform apply'}
    }
}
stage('Show') {
    node {
        withCredentials([[
            $class: 'AmazonWebServicesCredentialsBinding',
            credentialsId: credentialsId,
            accessKeyVariable: 'AWS_ACCESS_KEY_ID',
            secretKeyVariable: 'AWS_SECRET_ACCESS_KEY'
        ]]) {sh 'terraform show'}
    }
}
