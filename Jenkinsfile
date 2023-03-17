#!/bin/bash

  stage ('Test Stage 1') {
    withCredentials([[$class: 'UsernamePasswordMultiBinding',
                      credentialsId: "james372"
                      usernameVariable: 'AUSER'
                      passwordVariable: 'APASSWORD']]) {
      
      try {
        sh ''' #!/bin/bash
        echo "Hello"
        }
       }
      }
