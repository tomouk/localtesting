#!/bin/bash
node("master") {

  stage ('Test Stage 1') {
    withCredentials([[$class: 'UsernamePasswordMultiBinding',
                      credentialsId: "james372",
                      usernameVariable: 'AUSER',
                      passwordVariable: 'APASSWORD']]) {
      
      try {
        sh ''' #!/bin/bash
        git clone https://$AUSER:$APASSWORD@https://github.com/tomouk/localtesting.git
        '''
      }
      catch(error) {
        echo "Stage Failed!"
        throw error
      }
        }
       }
}
