pipeline {
  agent any
  stages {
    stage('Log tool version') {
      parallel {
        stage('Log tool version') {
          steps {
            sh '''java --version
 



                          git --version'''
          }
        }

        stage('check for PM') {
          steps {
            fileExists 'pom.xml'
          }
        }

      }
    }

    stage('build with mavan') {
      steps {
        sh 'mvn compile test package'
      }
    }

    stage('Build post step') {
      steps {
        writeFile(file: 'status.txt', text: 'it\'s  work fine')
      }
    }

  }
}