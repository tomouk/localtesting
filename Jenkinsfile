#!/bin/bash
node("master") {

  stage ('Test Stage 1') {
 //  withCredentials([[$class: 'UsernamePasswordMultiBinding',
 //                     credentialsId: "james372",
 //                     usernameVariable: 'AUSER',
 //                     passwordVariable: 'APASSWORD']]) {
      
      try {
        sh ''' #!/bin/bash
        rm -rf localtesting
        #git clone https://$AUSER:$APASSWORD@github.com/tomouk/localtesting.git
        git clone git@github.com:tomouk/localtesting.git
        echo Hello
        id
        ls -l
        cd localtesting
        ls
        cd playbooks
        ls -l
        '''
      }
      catch(error) {
        echo "Stage Failed!"
        throw error
      //}
        }
       }
}
