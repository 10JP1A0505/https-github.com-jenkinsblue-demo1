node {
    stage 'Download-SCM'
    git 'https://github.com/10JP1A0505/mavenrepo.git'
    stage 'Maven Compile'
    tool name: 'MAVEN-3.5.0', type: 'maven'
    sh 'mvn clean compile package deploy'
    stage 'ENV Dev Deploy'
    sh '''
    cd /var/lib/jenkins/ansible
    ansible-playbook -i DEVAPP -u ec2-user --private-key ec2-user.pem STUDENT-DEV-APP-DEPLOY.yml
    '''
}
