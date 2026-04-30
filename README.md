<img width="494" height="383" alt="image" src="https://github.com/user-attachments/assets/fbd43937-737e-4a01-ab30-4051842c5390" /># OS-Linux-commands-Shell-scripting
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
<img width="373" height="156" alt="image" src="https://github.com/user-attachments/assets/5c67a0c6-7954-4a78-9da2-55f8cd04a992" />



cat < file2
## OUTPUT
<img width="435" height="185" alt="image" src="https://github.com/user-attachments/assets/022d8312-16b5-4d51-85e1-90b9346fe6da" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="451" height="237" alt="image" src="https://github.com/user-attachments/assets/ce47df14-fe07-4187-9290-1d9d36bae5a2" />
 
comm file1 file2
 ## OUTPUT
<img width="516" height="228" alt="image" src="https://github.com/user-attachments/assets/2123372f-5b71-49f9-a3bc-a20058147344" />

 
diff file1 file2
## OUTPUT
<img width="521" height="272" alt="image" src="https://github.com/user-attachments/assets/b9918c5d-0569-4b43-bcd2-b97ec01a65e5" />


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
<img width="307" height="92" alt="image" src="https://github.com/user-attachments/assets/f37716d6-b76c-4bf0-b412-cca47e7efedd" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="505" height="127" alt="image" src="https://github.com/user-attachments/assets/6c5e8b56-ecf0-46bb-a804-55fc0e435d55" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="418" height="141" alt="image" src="https://github.com/user-attachments/assets/a20b59b2-729b-402f-ad27-2ce9518f7b16" />


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



grep hello newfile 
## OUTPUT




grep -v hello newfile 
## OUTPUT
<img width="308" height="83" alt="image" src="https://github.com/user-attachments/assets/48942b39-4185-49e8-afaf-f5d5c2ffbb3d" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="422" height="92" alt="image" src="https://github.com/user-attachments/assets/43b5b6a0-f1fc-4194-b58c-b0117f7ee417" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="452" height="77" alt="image" src="https://github.com/user-attachments/assets/e582c940-87e3-4e9e-8206-5863ce139df5" />




grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT
<img width="533" height="100" alt="image" src="https://github.com/user-attachments/assets/6180bbea-e310-4bb2-adb5-284ebf552f7e" />


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
<img width="553" height="233" alt="image" src="https://github.com/user-attachments/assets/ac2ce89d-9d2a-4623-a3d8-dc2fb78074c6" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
cat > newfile
<img width="585" height="106" alt="image" src="https://github.com/user-attachments/assets/c9dbf3a2-4c9f-4b01-b134-e4d78c15010e" />















egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="533" height="107" alt="image" src="https://github.com/user-attachments/assets/4e93bad2-14b3-4874-a175-49154e9e940b" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="552" height="84" alt="image" src="https://github.com/user-attachments/assets/d62cd720-0aaa-4ec7-bce6-671f3f02592d" />



egrep '(world$)' newfile 
## OUTPUT
<img width="602" height="119" alt="image" src="https://github.com/user-attachments/assets/212927f1-5bc9-4de0-a00e-b4ed59e598bf" />



egrep '(World$)' newfile 
## OUTPUT
<img width="665" height="77" alt="image" src="https://github.com/user-attachments/assets/27a3be7f-8135-41b2-9ffc-524b9e31737b" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="556" height="114" alt="image" src="https://github.com/user-attachments/assets/d056cc33-d594-42fb-8810-a534e9f1cdec" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="593" height="83" alt="image" src="https://github.com/user-attachments/assets/43e5c1f9-fa8d-49b1-a257-4c09e966ad46" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="555" height="51" alt="image" src="https://github.com/user-attachments/assets/5d676b8d-1ff9-4472-939b-3c04368fcebd" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="503" height="81" alt="image" src="https://github.com/user-attachments/assets/12102709-25ce-4a94-95d9-6fc538a4fccc" />


egrep l{2} newfile
## OUTPUT
<img width="526" height="114" alt="image" src="https://github.com/user-attachments/assets/e9fc6d06-7540-4118-a6a2-f57e0db4eec9" />



egrep 's{1,2}' newfile
## OUTPUT 
egrep 's{1,2}' newfile
<img width="581" height="143" alt="image" src="https://github.com/user-attachments/assets/bb8a3e4a-d0a0-49a1-b416-205a8e807f76" />

cat > file23
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


sed -n -e '3p' file23
## OUTPUT
<img width="628" height="83" alt="image" src="https://github.com/user-attachments/assets/e63d6568-b8b8-4a3f-871b-61cbef62ac40" />



sed -n -e '$p' file23
## OUTPUT
<img width="585" height="89" alt="image" src="https://github.com/user-attachments/assets/11034a78-b8a5-4cf0-bf23-c89689e7fdb4" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="746" height="278" alt="image" src="https://github.com/user-attachments/assets/f7c84a2b-5f98-4105-88dc-f1d49d59857a" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="614" height="284" alt="image" src="https://github.com/user-attachments/assets/6accc680-d2f6-4c78-9fdb-b3094349ff56" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="536" height="266" alt="image" src="https://github.com/user-attachments/assets/509155b4-d88f-449c-85d5-fa0fabe8f716" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="537" height="183" alt="image" src="https://github.com/user-attachments/assets/293057c7-11f3-4f97-bb76-8f9d1eb31b88" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="557" height="125" alt="image" src="https://github.com/user-attachments/assets/c3fca91c-2d65-4769-a19c-caf58129b7b8" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="493" height="114" alt="image" src="https://github.com/user-attachments/assets/142ae3cc-8916-44d7-b809-fb3fe139942d" />



seq 10 
## OUTPUT
<img width="764" height="309" alt="image" src="https://github.com/user-attachments/assets/6f7c3438-c97c-4f11-84b8-c48e3e4d4715" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="666" height="128" alt="image" src="https://github.com/user-attachments/assets/c76f4fb5-85fa-4047-835b-4fdd2646a0b6" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="643" height="136" alt="image" src="https://github.com/user-attachments/assets/4a305e96-bc99-4376-8669-bcb957ab44b7" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="674" height="160" alt="image" src="https://github.com/user-attachments/assets/a4cb268a-20ad-4a64-9c07-c3c633e713f4" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="564" height="143" alt="image" src="https://github.com/user-attachments/assets/2c751599-199c-4d26-9c98-6750fa5374cb" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="666" height="126" alt="image" src="https://github.com/user-attachments/assets/569ae266-e451-46dd-9d77-b3344fda0198" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
sed -n '2,4{s/^/$/;p}' file23
<img width="518" height="115" alt="image" src="https://github.com/user-attachments/assets/00f058d7-738e-4d71-919f-e16b11cfce60" />


sed -n '2,4{s/$/*/;p}' file23
<img width="597" height="138" alt="image" src="https://github.com/user-attachments/assets/698e6a62-854a-4a81-83e2-c8efce8b9c2f" />


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
<img width="523" height="168" alt="image" src="https://github.com/user-attachments/assets/bca468a2-e4a6-421d-8535-1e83915151c1" />


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
<img width="591" height="181" alt="image" src="https://github.com/user-attachments/assets/44c49e06-ae4d-4f7f-8a9d-70226cbc5958" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="503" height="287" alt="image" src="https://github.com/user-attachments/assets/2c60d50e-0538-43a3-b29e-8f2d69408333" />

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
<img width="515" height="130" alt="image" src="https://github.com/user-attachments/assets/ff40b2ed-ef22-4246-88ec-57154c75301d" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="652" height="137" alt="image" src="https://github.com/user-attachments/assets/77bfcaab-3e65-4dea-99f4-24f39a623d08" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="733" height="515" alt="image" src="https://github.com/user-attachments/assets/887ecddb-5d51-46cc-91ca-35a7dbae85ff" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="716" height="560" alt="image" src="https://github.com/user-attachments/assets/fed8a93c-c4ec-4ad2-ae77-3e58707ecbb5" />


tar -xvf backup.tar
## OUTPUT
<img width="731" height="508" alt="image" src="https://github.com/user-attachments/assets/5616acbe-0f56-4977-9182-6aa749c76787" />

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="642" height="145" alt="image" src="https://github.com/user-attachments/assets/216f7a5a-ff0c-4bd0-88b7-398be6b62707" />


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
<img width="703" height="559" alt="image" src="https://github.com/user-attachments/assets/0983eab4-d765-41f4-89e4-ecbf7f9201dc" />

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
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
##OUTPUT



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="667" height="141" alt="image" src="https://github.com/user-attachments/assets/ce62f7dc-9530-490e-ab23-27d2263f677e" />


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
<img width="636" height="85" alt="image" src="https://github.com/user-attachments/assets/9139a5e8-0643-455a-8c30-65fa4b12019d" />

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
<img width="659" height="139" alt="image" src="https://github.com/user-attachments/assets/361062d7-fcf2-4ddb-a302-b1461e624775" />



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
##OUTPUT
<img width="669" height="155" alt="image" src="https://github.com/user-attachments/assets/2356f116-1a7a-466b-908e-cedd0c82a43c" />

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
##OUTPUT

# looking for a possible value using elif
cat elifcheck.sh clear
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
<img width="692" height="608" alt="image" src="https://github.com/user-attachments/assets/fe44ca2e-bf4f-40d2-a8f9-9ba2063b38e8" />


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
clear
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
 
$ chmod 755 forin2.sh
 
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
 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
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
Basarac
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT


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
## OUTPUT

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
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


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



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
## OUTPUT
 ./funcex.sh 

 
 ./funcex.sh 1 2

 
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
 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```cdd
## OUTPUT
 ./argshift.sh 1 2 3
 
 
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

<img width="494" height="383" alt="image" src="https://github.com/user-attachments/assets/ab22f928-f86e-4827-aa21-ec27ccff1696" />

 
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

<img width="629" height="188" alt="image" src="https://github.com/user-attachments/assets/d78f35a1-adca-4830-ba37-2ed8e123185b" />


# RESULT:
The Commands are executed successfully.
