#!/bin/bash
node("master") {

  stage ('Test Stage 1') {
   // withCredentials([[$class: 'UsernamePasswordMultiBinding',
      withCredentials([[$class: 'sshUserPrivateKeyMultiBinding',
     //                 credentialsId: "james372",
                        credentialsId: "jentogh",
       //               usernameVariable: 'AUSER',
         //             passwordVariable: 'APASSWORD']]) {
      
      try {
        sh ''' #!/bin/bash
        #git clone https://$AUSER:$APASSWORD@github.com/tomouk/localtesting.git
        git clone git@github.com:tomouk/localtesting.git
        echo Hello
        '''
      }
      catch(error) {
        echo "Stage Failed!"
        throw error
      }
        }
     //  }
}
