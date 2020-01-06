pipeline
{
    agent any
    stages
    {
        stage('FetchStage')
        {
            steps
            {
                git 'https://gitlab.com/calindoran/JenkinsProject'
            }
        }

        stage('BuildStage')
        {
            steps
            {
                bat 'javac -cp junit-4.13.jar; Student.java studentTest.java'
            }
        }

        stage('TestStage')
        {
            steps
            {
                bat 'java -cp junit-4.13.jar;hamcrest-core-1.3.jar; org.junit.runner.JUnitCore studentTest'
            }
        }
    }
}
