struts2-ejb-archetype
============

1. Git Clone the project: 
git clone https://github.com/dmouch/struts2-ejb-archetype.git

2. Install the archetype locally:
cd struts2-ejb-archetype && mvn clean install

3. Create new project from local archetype catalog:
mvn archetype:generate -DarchetypeCatalog=local

4. In root pom change "Database dependencies" appropriately:
<!-- Database dependencies -->
<version.jdbc.groupId>mysql</version.jdbc.groupId>
<version.jdbc.artifactId>mysql-connector-java</version.jdbc.artifactId>
<version.jdbc.version>5.1.30</version.jdbc.version>
<version.jdbc.driver>com.mysql.jdbc.Driver</version.jdbc.driver>

5. In ~/.m2/settings.xml in your default profile add required properties for database:
<project-name>.jdbc.admin.url
<project-name>.jdbc.admin.username
<project-name>.jdbc.admin.password

<project-name>.jdbc.url
<project-name>.jdbc.username
<project-name>.jdbc.password

6. In <project-name>-sql/pom.xml change <dbCreateStatements> and <dbDropStatements> appropriately

