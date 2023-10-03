pipeline {
	agent {
		label "Pipeline-slave"
	}
	stages{
		stage ("pull scm"){
			steps {
				git branch: 'main', url: 'https://github.com/devsharma1401/testing.git'	
			}
		}
		stage ("Build"){
			steps {
				sh 'python3 -v'
				sh 'python3 cp.py'
			}
		}
		stage ("test" ){
			steps {
				sh 'python3 test.py'
			}
		}
	}
}
