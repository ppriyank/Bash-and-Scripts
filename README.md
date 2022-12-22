# hadoop
Concatenating partitions into one
```
hadoop fs -cat /path/to/the/file >> out.put.txt
```






# java: 
### Finding all jars
```
sudo find ./ -iname "*.jar"
```

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
echo "set enable-bracketed-paste off" >> ~/.inputrc
```

### If/else in a list

```
[i for i in sentence if ....]
```
```
[i if ... else ... for i in original_prices]
```

### GPU status 
```
python -c "import torch; print(torch.cuda.is_available()); print(torch.version.cuda) ; print(torch.__version__); print(torch.cuda.device_count())"

python -c "import torch; print(torch.__file__); print(torch.__version__); print(torch.cuda.device_count())"
```






# Bash
### Installing from anywhere
```
sudo spctl --master-disable
```
then disable `sudo spctl --master-enable`


### Correct configuration of .ssh/config 

```
chmod 600 ~/.ssh/config
```
### Correct ~/.ssh/config 

```
Host *
  IgnoreUnknown UseKeychain
  AddKeysToAgent yes
  UseKeychain yes
  IdentityFile ~/.ssh/id_rsa
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

Check status of each GPU `checkstatus.sh`  

```
truncate -s 0 status.txt

while read HOST ; 
do 
    ssh $HOST "echo $HOST >> status.txt ; nvidia-smi >> status.txt" < /dev/null ; 
done < servers.txt
```
`server.sh`  
```
gpu001
gpu002
```








# Github
https://github.com/ppriyank/Github-Tutorial/blob/master/README.md








# link of Commands 

```which java```
Pointing to actual path : 
```
ls -l `which java`
```





# Latex
Fonts: https://tex.stackexchange.com/questions/56008/different-sizes-of-font-available-in-table   







# Bash profile

`vim ~/.bashrc`   
`vim ~/.bash_profile`

```
conda activate pathak3
alias session="tmux new -s pathak; tmux a -t pathak"
alias gpus="watch nvidia-smi"
alias refresh='clear; reset; source ~/.bash_profile; source ~/.bashrc'
```

`refresh`


