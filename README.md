Maven is a versatile build automation tool widely employed in Java projects. It facilitates the transformation of source code into deployable artifacts, particularly War files for web applications. Maven operates on the foundation of a Project Object Model (POM) file, delineating project structure, dependencies, and build instructions. Developers commence with writing source code, typically in languages like Java or C++, and proceed to compile it. Following compilation, unit testing is conducted locally to ensure code integrity. Upon successful testing, the code is packaged into various formats such as JAR or WAR files for Java projects, or ZIP files for Python projects. Subsequently, developers perform a health check, analyzing the code for bugs and vulnerabilities. Maven is commonly integrated with Jenkins for automated build processes, leveraging Maven plugins to streamline artifact generation. Alternatively, developers can manually build the source code using Maven, installing it on an EC2 instance within an AWS environment. For instance, launching an EC2 instance running Ubuntu distribution allows for manual source code building with Maven.

To install Maven on an EC2 instance, start by connecting to the instance using SSH or EC2 Instance Connect. Switch to the root user for full permissions with the command **sudo su**. Begin by updating the system to install necessary dependencies using **apt update -y.**

Since Maven requires Java, install the Java Development Kit (JDK) with **apt install openjdk-11-jdk -y.** Verify the installed Java version using java -version.

To install the **default Maven version (3.6.3), execute apt install maven -y.** If a **different version, such as 3.9.6, is desired, download the corresponding tar file from the Apache Maven website**. Copy the tar file to the EC2 instance.

Navigate to the **/opt/ directory using cd /opt/**, and use **wget to download the Maven tar file**. Confirm the download with **ls -l**. **Extract the tar file with tar -xvf <tar file> and delete the tar file with rm -rf <tar file>.**

Enter the Apache Maven directory (e.g., **cd /apache-maven-3.9.6**) and explore its contents with ls. Move into the bin/ directory **(cd bin/)** and list its contents **(ls -l).**

Set the **Maven path with export PATH=$PATH:/opt/apache-maven-3.9.6/bin**. Verify the Maven installation by running **mvn -version.**
