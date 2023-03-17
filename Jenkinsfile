#!/bin/bash
node("master") {

  stage ('Test Stage 1') {
    withCredentials([[$class: 'UsernamePasswordMultiBinding',
                      credentialsId: "james372",
                      usernameVariable: 'AUSER',
                      passwordVariable: 'APASSWORD']]) {
      
      try {
        sh ''' #!/bin/bash
        yum update git -y
        git clone https://$AUSER:$APASSWORD@github.com/tomouk/localtesting.git
        '''
      }
      catch(error) {
        echo "Stage Failed!"
        throw error
      }
        }
       }
}
