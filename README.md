Shopizer 2.2.0 (for java 1.8)
-------------------

Java open source e-commerce software

- Shopping cart
- Catalogue
- Search
- Checkout
- Administration
- REST API


Pre-Requisites 
-------------------
 - Install JSK 8, application don't run witj JDK 10 which is the latest version. I tested with JDK version 1.8_191
 - Install Maven
 - Download Tomcat 9.0



Configure Maven
-------------------
 - Download maven in a directory 
 - Create a soft link using command below:

 	$ ln -s <path to maven>/bin/mvn /usr/bin/mvn

 - Test if maven was configured using command below:

	$ mvn -v


Configure Tomcat 
-------------------
 - Open catalina.sh in an editor and add below two lines. Add these lines at the top right when comments end, donot add them at the bottom of the file

 	$ JAVA_HOME='/Library/Java/JavaVirtualMachines/jdk1.8.0_191.jdk/Contents/Home'
	$ JAVA_OPTS="-Xms1024m -Xmx1024m -XX:MaxPermSize=256m"


To get the code:
-------------------
Clone the repository using Git Desktop




To build the application:
-------------------	
From the command line with Maven installed:

	$ cd shopizer
	$ mvn clean install
	

Run the application from Tomcat 
-------------------
copy sm-shop/target/ROOT.war to tomcat or any other application server deployment dir

Increase heap space to 1024 m or at least 512 m

### Heap space configuration in Tomcat:


If you are using Tomcat, edit catalina.bat for windows users or catalina.sh for linux / Mac users

	in Windows
	set JAVA_OPTS="-Xms1024m -Xmx1024m -XX:MaxPermSize=256m" 
	
	in Linux / Mac
	export JAVA_OPTS="-Xms1024m -Xmx1024m -XX:MaxPermSize=256m" 

Run the application from Spring boot 
-------------------

       $ cd sm-shop
       $ mvn spring-boot:run

Run the application from Spring boot in eclipse
-------------------

Right click on com.salesmanager.shop.application.ShopApplication

run as Java Application

### Access the application:
-------------------

Access the deployed web application at: http://localhost:8080/

Acces the admin section at: http://localhost:8080/admin

#####username : admin
#####password : password

The instructions above will let you run the application with default settings and configurations.
Please read the instructions on how to connect to MySQL, configure an email server and configure other subsystems


### Documentation:
-------------------

Documentation available from the wiki <http://shopizer-ecommerce.github.io/shopizer/#>

More information is available on shopizer web site here <http://www.shopizer.com>
