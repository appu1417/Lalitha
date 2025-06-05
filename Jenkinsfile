pipeline{
agent any
tools{
gradle 'gradle'
jdk 'JDK'
}
stages{
stage('Checkout'){
steps{
git branch:'master',url:'https://github.com/appu1417/Lalitha.git'
}
}
stage('Build'){
steps{
sh 'gradle build'
}
}
stage('Test'){
steps{
sh 'gradle test'
}
}
stage('Run Application'){
steps{
sh 'gradle run'
}
}
}
post{
success{
echo 'Build Success'
}
failure{
echo 'Build Failure'
}
}
}
