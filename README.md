# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/5ac59ed6-7f13-4b90-9ba1-e06c9079d38a)




cat < file2
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/6e750021-cb90-4a8b-9399-5cd683207055)



# Comparing Files
cmp file1 file2
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/06768d9a-5ecb-4e23-9bc1-7630a07e1214)

 
comm file1 file2
 ## OUTPUT
 ![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/396a60c6-48f8-43a2-b1da-5fc06ffb32dd)


 
diff file1 file2
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/1f47c143-1204-4e29-80c1-d18d1e78c935)



#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/d4cb7b17-d2a4-4d16-b897-4fd2867189d4)





cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/7717ad4d-cfa2-42d7-b667-05f0705de4fa)




cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/69d4c990-0d69-40f9-b080-5517c67c86ac)



cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/66f7064a-b6b0-4a8c-8a8e-94ffb952a3f3)




grep hello newfile 
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/f899a5a1-bf7c-4c56-8898-cda3d2568d70)





grep -v hello newfile 
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/6ece6b5c-faaf-4d5b-9e1a-83a2af6c6694)




cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/6b069fdb-4a2e-466c-aa1b-c8dfbcea58c7)





cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/18266256-066b-46b8-870f-5dd3dcb98fb4)





grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/a5c9bc31-6545-45ec-83e1-1966598b88ef)



cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/9b0d3817-2ad2-423f-9a08-796f27974de7)




egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/acf1ae58-f39d-454a-89c9-241afb5dfef2)




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/4aa6f5d1-2419-4146-a017-d5a1af822ead)





egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/c602e377-c739-4044-aac6-4536c51f3f16)




egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/eac8edb1-630b-440e-9eb8-1e04ea71b6a7)


egrep '(World$)' newfile 
## OUTPUT


![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/fbc0748a-3cd5-4a8e-bed7-eb68cca2d2af)


grep '((W|w)orld$)' newfile 

## OUTPUT

![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/9a059747-b312-4711-a99a-23b571d07209)



egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/719de72b-95fc-4f95-9f7e-d5ac2c90b80a)


egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/e827e438-13df-4be2-835c-535ab9e37566)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/2c4b5ac2-cd7e-48ce-92d3-b15eaaae9117)


egrep l{2} newfile
## OUTPUT

![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/fd348c60-d7d6-45cd-8bdd-603438b6e50a)


egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/13d40e23-b816-465b-bea4-8458318d4d67)



cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file22
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/6d5eaecf-68d9-4ef0-896f-5a3f05c655ab)


sed -n -e '$p' file22
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/f35d4d48-6910-4736-b1f8-24c6445a6755)




sed -e 's/Ram/Sita/' file22
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/b2543fcd-85a6-44dd-820c-0f34c7135a0a)




sed -e '2s/Ram/Sita/' file22
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/9ccff721-5b9b-4062-8e84-2f28e09e6484)




sed  '/tom/s/5000/6000/' file22
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/42d9d27f-7a36-48aa-84cd-6e3115ac60d8)



sed -n -e '1,5p' file22
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/87b522e8-f576-44cb-9107-51ad25b64de3)




sed -n -e '2,/Joe/p' file22
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/6a221105-5562-4237-84a0-ac61d143a68f)





sed -n -e '/tom/,/Joe/p' file22
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/d2b4e450-619a-4e1d-8d08-e8e72d938e9b)




seq 10 
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/e223a991-5737-484d-8bd7-efbe548f5fe6)




seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/f19bbd24-4555-4543-9607-5d0a61bc5eff)




seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/0fd290f7-9a24-4d40-80ed-ad40cb0cdc51)




seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/4e34278d-9f5b-4eaf-9d12-1327b2f0e059)




seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/4ab9685a-79ac-41ba-a8ab-934155f8a48c)



seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/e64a986a-7caf-45c9-bb5a-e57360f3842c)



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/4eea9265-c182-4d03-9157-0d25dd65c126)




sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/94374bf0-7d14-4b96-bcdd-882e374aa573)



#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/2e89960b-eb67-4dd7-a21e-e504043237eb)



cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/7695d682-4226-4f13-b7f3-276dfa94d108)




#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 ![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/4d7d0879-e1d0-4b1f-ad29-8c4ab7758476)


cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
 ![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/27bc572c-4a1b-42e2-b2c2-30af210b8a51)



 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/d3cfbfe2-a179-4913-b98c-52ccb8067fef)




#Backup commands
tar -cvf backup.tar *
## OUTPUT
```
bench.py
file1
file11
file2
file21
file22
file23
hello.c
hello.js
newfile
readme.txt
urllist.txt
```


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
```
-rw-r--r-- user/group 0 2024-02-25 14:30:00 file1.txt
drwxr-xr-x user/group 0 2024-02-25 14:30:00 directory1/
-rw-r--r-- user/group 1024 2024-02-25 14:30:00 directory1/file2.txt
-rw-r--r-- user/group 2048 2024-02-25 14:30:00 directory1/file3.txt
```


tar -xvf backup.tar
## OUTPUT
```
x file1.txt
x directory1/
x directory1/file2.txt
x directory1/file3.txt
```

gzip backup.tar

ls .gz
## OUTPUT
```
 backup.tar.gz
```
 
gunzip backup.tar.gz
## OUTPUT
```
backup.tar
```
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/4ac7c3f8-515f-41f4-9d1b-5daa8c797c62)


 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/c4b0df17-78fc-4418-87ed-fdeed2df6ea7)



cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
```
File name is ./scriptest.sh
File name is scriptest.sh
First arg. is 1
Second arg. is 2
Third arg. is 3
Fourth arg. is
The $@ is 1 2 3
The $\# is $#
The $$ is 124
```

 
ls file1
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/4a54fa9f-d0f5-42aa-b603-f7f75ef97bb1)


echo $?
## OUTPUT 
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/c580b5c8-d841-46f9-b95c-370fb6efd4fe)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT
 1


 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/24e70162-c2aa-4f1f-8a86-9ee6c9e90d93)




chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
```
baseball is less than hockey
```


# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT
```
You are the owner of the /etc/passwd file
```
# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/e293359c-6ec2-43f2-8dd4-3744a5b8ff37)



# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/9721458f-dc5e-4480-a366-239c230dbb10)


# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/9870a9f4-7e7a-487d-a9d4-044d115f02e8)


# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT
```
Welcome Ram
Please enjoy your visit
Welcome Rahim
Please enjoy your visit
Special testing account
gganesh, Do not forget to logout when you're done
Sorry, you are not allowed here
```


# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT
![image](https://github.com/PRASHANTHRATHI/OS-Linux-commands-Shell-script/assets/145743120/b5046158-59a3-4dcf-bc60-67cea72d83ee)

# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
## OUTPUT
```
Welcome Ram/Rahim
Please enjoy your visit
Special testing account
gganesh, Do not forget to logout when you're done
Sorry, you are not allowed here
```
 
cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
## OUTPUT
```
10
9
8
7
6
5
4
3
2
1
```
 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
## OUTPUT
```
100
75
50
25
```
 
 
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh $ ./forin1.sh
## OUTPUT
```
The next state is Alabama
The next state is Alaska
The next state is Arizona
The next state is Arkansas
The next state is California
The next state is Colorado
```
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
## OUTPUT
```
word:I
word:dont know if thisll
word:work
```
 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ ./forin3.sh

## OUTPUT
```
word:I
word:don't
word:know
word:if
word:this'll
word:work
```

cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT
```
Visit beautiful Hyderabad
Visit beautiful Alampur
Visit beautiful Basara
Visit beautiful Warangal
Visit beautiful Adilabad
Visit beautiful Bhadrachalam
Visit beautiful Khammam
```


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT
```
The value of i is 1
The value of i is 2
The value of i is 3
The value of i is 4
The value of i is 5
```

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT

cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT
 ```
1 - 5
2 - 4
3 - 3
4 - 2
5 - 1
```

 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
$ chmod 755 forbreak.sh$ ./forbreak.sh 
## OUTPUT
```
Iteration number: 1
Iteration number: 2
The for loop is completed
```
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
```
Iteration number: 1
Iteration number: 2
Iteration number: 4
Iteration number: 5
The for loop is completed
```
 
cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT
```
Enter your name: John
Hello John, welcome to my program.
```


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
```
Enter your name: sanju
Hello sanju, welcome to my program.
```



$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
 ./funcex.sh 

 
 ./funcex.sh 1 2
## OUTPUT
 ```
$ bash script.sh 1 2
The result is 2
```

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3
```
1
2
3
```
 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
$ ./argshift.sh 1 2 3
```
1
2
3
```
 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
```
+ (( 0 ))
+ set +x
```
 
 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
```
total characters 75
Number of Lines are 10
No of Words count: 10
```
 
cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 
```
Enter the number
121
Number is palindrome
Enter the number
69
Number is NOT palindrome
```


# RESULT:
The Commands are executed successfully.







