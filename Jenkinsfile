node {
    stage 'Download-SCM'
    git 'https://github.com/carreerit/mavenrepo.git'
    stage 'Maven Compile'
    tool name: 'MAVEN-3.5.0', type: 'maven'
    sh 'mvn clean compile package deploy'
    
}
