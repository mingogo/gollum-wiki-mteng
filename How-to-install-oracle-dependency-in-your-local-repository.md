How do I find a repository (if any) that contains this artifact?

Unfortunately due the binary license there is no public repository with the Oracle Driver JAR. This happens with many dependencies but is not Maven's fault. If you happen to find a public repository containing the JAR you can be sure that is illegal.

How do I add it so that Maven will use it?

Some JARs that can't be added due to license reasons have a pom entry in the Maven Central repo. Just check it out, it contains the vendor's preferred Maven info:

<groupId>com.oracle</groupId>
<artifactId>ojdbc14</artifactId>
<version>10.2.0.3.0</version>
...and the URL to download the file which in this case is http://www.oracle.com/technology/software/tech/java/sqlj_jdbc/index.html.

Once you've downloaded the JAR just add it to your computer repository with (note I pulled the groupId, artifactId and version from the POM):

```
mvn install:install-file -DgroupId=com.oracle -DartifactId=ojdbc14 -Dversion=10.2.0.3.0 -Dpackaging=jar -Dfile=ojdbc.jar -DgeneratePom=true
```
The last parameter for generating a POM will save you from pom.xml warnings

If your team has a local Maven repository this guide might be helpful to upload the JAR there.