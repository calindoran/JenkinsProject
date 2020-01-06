pipeline
{
    agent any
    stages
    {
        stage('Fetch')
        {
            steps
            {
                git url:'https://gitlab.com/calindoran/JenkinsProject.git'
            }
        }

        stage('Build')
        {
            steps
            {
                bat 'javac -cp junit-4.13.jar; Student.java studentTest.java'
            }
        }

        stage('Test')
        {
            steps
            {
                bat 'java -cp junit-4.13.jar;hamcrest-core-1.3.jar; org.junit.runner.JUnitCore studentTest'
            }
        }
    }
}
