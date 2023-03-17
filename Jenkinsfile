#!/bin/bash
node(master) {

  stage ('Test Stage 1') {
    withCredentials([[$class: 'UsernamePasswordMultiBinding',
                      credentialsId: "james372",
                      usernameVariable: 'AUSER',
                      passwordVariable: 'APASSWORD']]) {
      
      try {
        sh ''' #!/bin/bash
        echo "Hello"
        '''
      }
      catch(error) {
        echo "Stage Failed!"
        throw error
      }
        }
       }
}
