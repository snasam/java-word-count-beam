# java-word-count-beam
Apache Beam

## Steps to set up your environment
Download and install the Java Development Kit (JDK) version 8. Verify that the JAVA_HOME environment variable is set and points to your JDK installation
Download and install Apache Maven by following Maven’s installation guide for your specific operating system.
Optional: Install Gradle if you would like to convert your Maven project into Gradle.

## Get the example code
mvn archetype:generate `
 -D archetypeGroupId=org.apache.beam `
 -D archetypeArtifactId=beam-sdks-java-maven-archetypes-examples `
 -D archetypeVersion=2.36.0 `
 -D groupId=org.example `
 -D artifactId=word-count-beam `
 -D version="0.1" `
 -D package=org.apache.beam.examples `
 -D interactiveMode=false
 
 PS> cd .\word-count-beam
 PS> dir
 
 ## Optional: Convert from Maven to Gradle Project
 $ gradle init
 
 ## Building the project and running using the command
 $ gradle build
 
## Run WordCount Using Maven
mvn compile exec:java -D exec.mainClass=org.apache.beam.examples.WordCount `
 -D exec.args="--inputFile=sample.txt --output=counts" -P direct-runner
 
 ## Run WordCount Using Gradle
 $ gradle clean execute -DmainClass=org.apache.beam.examples.WordCount \
    -Dexec.args="--inputFile=sample.txt --output=counts" -Pdirect-runner
    
 ## Inspect the results
 $ ls counts*
