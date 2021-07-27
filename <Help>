node('master') {
   stage('scm') {
       git 'https://github.com/hawlette/openmrs-core.git'
   }
   stage('maven'){
     sh 'mvn clean package'
   }
   stage('postbuild'){
        junit '**/TEST-*.xml'
         archive '**/* .war'
   }
   
}
