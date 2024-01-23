# Update you packager manager
sudo yum update

# Install openjdk
sudo yum install java-11-amazon-corretto

# Verify java
java --version

# Download Apache Maven
wget https://dlcdn.apache.org/maven/maven-3/3.9.6/binaries/apache-maven-3.9.6-bin.tar.gz

# Extract tar file
tar xzvf apache-maven-3.9.6-bin.tar.gz

# Move the ectracted file into desired location
sudo mv apache-maven-3.9.6 /opt its already exits, choose different sudo mv apache-maven-3.9.6 /opt/maven-3.9.6

# Setup environment
export JAVA_HOME="/usr/lib/jvm/java-11-amazon-corretto"
export MAVEN_HOME="/opt/maven-3.9.6"
export PATH="$PATH:$HOME/bin:$JAVA_HOME/bin:$MAVEN_HOME/bin"

# Save the file and run
source ~/.bash_profile
source ~/.bashrc

# Verify maven
mvn --version
