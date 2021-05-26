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

### Running mutiple python commands w/o shell

```
python -c "import tools.data_manager as data_manager; dataset = data_manager.init_dataset(name="cuhk01")"
```

# Bash

### Correct configuration of .ssh/config 

```
chmod 600 ~/.ssh/config
```

### Finding a file : 
```sudo find / -iname "dist-packages"```

#### Size of a folder (on hdfs): 
```hadoop fs -du -s -h /user/ppathak/```

### Size of a fodler 
```du -s -h ./```

### Number of files in a folder: 
```
find /etc -type f | wc -l
```
### Problems with mounting :
```
pgrep -lf sshfs
kill -9 <pid_of_sshfs_process>
sudo umount -f <mounted_dir>
```

### ssh-ing using password & tunnels : 
```
sshpass -p <password here> ssh -f pp1953@gw.hpc.nyu.edu -L 5556:greene.hpc.nyu.edu:22 -N
sshpass -p <password here> ssh -p 5556 pp1953@127.0.0.1
```
Do not use sshpass for sshfs
```
sshfs -p 5556 pp1953@127.0.0.1:/home/pp1953/reid ~/NYU/project2
```



# link of Commands 

```which java```
Pointing to actual path : 
```
ls -l `which java`
```
