node(){
    
    stage("Clone"){
        echo "Clone"
        checkout changelog: false, poll: false, scm: [$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/csenapati12/java-tomcat-maven-docker.git']]]
    }
      stage("Bhuild and Packaging"){
        echo "Build and Packaging"
        sh 'mvn package'
    }
      stage("Nexus Upload"){
        echo "Nexus"
          sh """
          cd target
          ls -la
          """
       // sh 'mvn deploy'
    }
      stage("Sonar analysis"){
        echo "Sonar"
      
    }  
    stage("Docker"){
        echo "Docker"
    }
}
