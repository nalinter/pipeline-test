
def cancelbuilds(){
	def jobName = env.JOB_NAME
	echo "${jobName}"
    def buildNumber = env.BUILD_NUMBER.toInteger()
	echo "${buildNumber}"
    def currentJob = Jenkins.instance.getItemByFullName(jobName)
	echo "${currentJob}"

}



pipeline{
  agent any
  stages{
    stage("sample"){
      steps{
	      script{
		      def json = currentBuild.getBuildCauses()
		      def type = json.getClass()
		      echo "${type}"
	      	      def author = json.get(3)
		      def userid = json.get(4)
		      echo "author : ${author}"
		      echo "userid : ${userid}"
	      }
      }
    }
  }
}
