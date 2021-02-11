# hadoop
Concatenating partitions into one
```
hadoop fs -cat /path/to/the/file >> out.put.txt
```

# java: 

### mutiple jars
```
jar cvf xyz.jar folder/of/all/*.class
javac -cp  :folder_of_all_jars/* abcd.java 
java -cp ":folder_of_all_jars/*" abcd

```

Path of java library 
```
 /usr/libexec/java_home -V
 ```
 
### Scala-java
https://spark.apache.org/docs/2.1.0/sql-programming-guide.html

### All jars:
https://repo1.maven.org/maven2/

# Python


# Bash
Finding a file : 
```sudo find / -iname "dist-packages"```

Size of a folder (on hdfs): 
```hadoop fs -du -s -h /user/ppathak/```

Size of a fodler 
```du -s -h ./```

# link of Commands 

```which java```
Pointing to actual path : 
```
ls -l `which java`
```
