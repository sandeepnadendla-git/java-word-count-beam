# java-word-count-beam
# The following are the step by step commands i used to create and run this

mvn archetype:generate `
 -D archetypeGroupId=org.apache.beam `
 -D archetypeArtifactId=beam-sdks-java-maven-archetypes-examples `
 -D archetypeVersion=2.36.0 `
 -D groupId=org.example `
 -D artifactId=word-count-beam `
 -D version="0.1" `
 -D package=org.apache.beam.examples `
 -D interactiveMode=false

cd .\word-count-beam

dir

dir .\src\main\java\org\apache\beam\examples

I got an issue with my java since i am using jdk 12 so installed java jdk11 using chocolatey
 
 choco install openjdk11 -y

mvn compile exec:java -D exec.mainClass=org.apache.beam.examples.WordCount -D exec.args="--inputFile=sample.txt --output=counts" -P direct-runner

ls count*

more count*