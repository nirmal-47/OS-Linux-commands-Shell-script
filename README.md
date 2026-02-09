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
<img width="975" height="210" alt="image" src="https://github.com/user-attachments/assets/5c09057a-0619-44d8-873e-d0fb5a4ac27e" />



cat < file2
## OUTPUT
<img width="980" height="243" alt="image" src="https://github.com/user-attachments/assets/0d8b9bd8-da2a-4ca0-b357-5a545387b04b" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="980" height="105" alt="image" src="https://github.com/user-attachments/assets/8352035f-9564-4837-8f30-13cc0a263a01" />

comm file1 file2
 ## OUTPUT

<img width="975" height="308" alt="image" src="https://github.com/user-attachments/assets/f35aafe7-e40f-4774-babb-372513416f52" />

diff file1 file2
## OUTPUT


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
<img width="970" height="138" alt="image" src="https://github.com/user-attachments/assets/d5d4124d-ae6b-4a58-8ddb-498c2e2e1624" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="975" height="173" alt="image" src="https://github.com/user-attachments/assets/137059a5-67ba-4d89-b1d4-915b81e0ee13" />

cut -d "|" -f 2 file22
## OUTPUT
<img width="968" height="166" alt="image" src="https://github.com/user-attachments/assets/c97962d4-8594-4b51-8cd7-71bc9bbe8455" />


cat > newfile 
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
<img width="982" height="107" alt="image" src="https://github.com/user-attachments/assets/5bf51c48-77c4-42dd-bc67-46e71b14a5a5" />


grep hello newfile 
## OUTPUT
<img width="976" height="105" alt="image" src="https://github.com/user-attachments/assets/9b5957a9-cefa-4a1f-a31f-213a7986dd92" />



grep -v hello newfile 
## OUTPUT
<img width="968" height="101" alt="image" src="https://github.com/user-attachments/assets/6fc2613d-69e7-4622-8738-c91ec6b88390" />


cat newfile | grep -i "hello"
## OUTPUT
<img width="976" height="136" alt="image" src="https://github.com/user-attachments/assets/1d992867-45fb-4efa-b565-64bae9053eff" />



cat newfile | grep -i -c "hello"
## OUTPUT
<img width="977" height="108" alt="image" src="https://github.com/user-attachments/assets/a02a1dae-38b4-48c2-9bd7-23afd58991ff" />



grep -R ubuntu /etc
## OUTPUT
<img width="1887" height="778" alt="image" src="https://github.com/user-attachments/assets/ed484bb1-4d30-4132-a546-690c10e8b14e" />



grep -w -n world newfile   
## OUTPUT
<img width="1030" height="140" alt="image" src="https://github.com/user-attachments/assets/7a019d32-0d2a-4d42-bc94-5680cf702bd3" />

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
<img width="977" height="139" alt="image" src="https://github.com/user-attachments/assets/59963575-e5b3-4e6f-8f6c-1ebb3132beb6" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="977" height="138" alt="image" src="https://github.com/user-attachments/assets/3794c35f-de6d-40b7-82c2-00f1abb46bf2" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="970" height="137" alt="image" src="https://github.com/user-attachments/assets/56c9afb6-73a1-41c7-a6c3-3985a06fae14" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="973" height="103" alt="image" src="https://github.com/user-attachments/assets/1a53071b-3729-4198-91b9-403da6867953" />



egrep '(world$)' newfile 
## OUTPUT
<img width="973" height="138" alt="image" src="https://github.com/user-attachments/assets/cfe87dfa-a3d3-4b50-915b-4eddf4526c33" />


egrep '(World$)' newfile 
## OUTPUT
<img width="968" height="99" alt="image" src="https://github.com/user-attachments/assets/3206f5da-3d9f-484a-b021-eb6a3121c31a" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="977" height="170" alt="image" src="https://github.com/user-attachments/assets/5869bb0b-b268-4b67-8fb1-89e47a22afa5" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="985" height="105" alt="image" src="https://github.com/user-attachments/assets/ac9b63d4-da64-4367-8352-436706714fcb" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="972" height="100" alt="image" src="https://github.com/user-attachments/assets/c93df48d-7f70-42ba-8702-a34777a5eff0" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="972" height="104" alt="image" src="https://github.com/user-attachments/assets/9f5b3272-2474-42b4-97f9-f38d11f10cc4" />

egrep l{2} newfile
## OUTPUT
<img width="976" height="140" alt="image" src="https://github.com/user-attachments/assets/d66eea69-a9e1-41cb-a7fc-f081935cf4d4" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="968" height="164" alt="image" src="https://github.com/user-attachments/assets/9c1e91cf-aa7c-4423-adfc-e85729ce03e5" />


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
<img width="967" height="104" alt="image" src="https://github.com/user-attachments/assets/83657402-ec44-4a66-b693-4c5a597d9da1" />



sed -n -e '$p' file23
## OUTPUT
<img width="982" height="99" alt="image" src="https://github.com/user-attachments/assets/45ed80c6-372d-4fe5-84ea-6a0abdd1843e" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="970" height="339" alt="image" src="https://github.com/user-attachments/assets/6a77e99f-274e-4c08-a8c2-8d4d3dea8585" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="975" height="335" alt="image" src="https://github.com/user-attachments/assets/582adc17-e376-40b3-9fa5-88a443f814ea" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="970" height="345" alt="image" src="https://github.com/user-attachments/assets/802f9c32-7214-4ad0-8c95-dde9283a1cc1" />


sed -n -e '1,5p' file23
## OUTPUT
<img width="977" height="247" alt="image" src="https://github.com/user-attachments/assets/cfb77dfa-6be8-4dcf-9a61-ce83db4a198c" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="982" height="170" alt="image" src="https://github.com/user-attachments/assets/d0fd0d23-75e6-460a-9815-381d3119a4e4" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="976" height="135" alt="image" src="https://github.com/user-attachments/assets/d6c9c9f8-a0fe-4c71-a9d6-f060a02257e1" />


seq 10 
## OUTPUT
<img width="980" height="410" alt="image" src="https://github.com/user-attachments/assets/e5291da0-fe2f-4e64-9801-ae8aaf3cbb50" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="971" height="172" alt="image" src="https://github.com/user-attachments/assets/c76c4016-ae2c-44cb-91d3-935f5b851978" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="977" height="173" alt="image" src="https://github.com/user-attachments/assets/4afa90bf-dd61-4905-a58d-2e25741bd17a" />


seq 3 | sed '2a hello'
## OUTPUT
<img width="991" height="202" alt="image" src="https://github.com/user-attachments/assets/c3b95b1b-f3f9-4930-bb32-f94dff83a10d" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="976" height="165" alt="image" src="https://github.com/user-attachments/assets/3db00942-c8c9-492c-a0e8-16cdfe4a96ec" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="977" height="170" alt="image" src="https://github.com/user-attachments/assets/91626708-f661-4b80-a7e5-5fd1b53a8bd4" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="986" height="172" alt="image" src="https://github.com/user-attachments/assets/b2a6e6f8-0ab9-45db-8405-acd5deb928f9" />



sed -n '2,4{s/$/*/;p}' file23
<img width="980" height="169" alt="image" src="https://github.com/user-attachments/assets/7dc104e0-0182-41d7-b8f0-e42d97b8daa0" />


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
<img width="972" height="238" alt="image" src="https://github.com/user-attachments/assets/e5449512-07d3-4fae-b50f-3709bdb30517" />


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
<img width="971" height="239" alt="image" src="https://github.com/user-attachments/assets/596ead0b-0ac7-4139-9bd7-3b4d05653605" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="978" height="341" alt="image" src="https://github.com/user-attachments/assets/61b65b5f-2fe4-4158-829b-a465654345e3" />

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
<img width="983" height="179" alt="image" src="https://github.com/user-attachments/assets/8c18480e-f9c1-483a-a21e-ea509a6fcec6" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="973" height="170" alt="image" src="https://github.com/user-attachments/assets/198a20e1-2001-4256-b979-a44d564468a8" />


#Backup commands
<img width="973" height="170" alt="image" src="https://github.com/user-attachments/assets/012cba61-2554-4c54-84f8-e01c74e7897d" />

tar -cvf backup.tar *
## OUTPUT

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="1112" height="341" alt="image" src="https://github.com/user-attachments/assets/2ef6fe49-727a-4cef-a615-89aa659e8b0e" />


tar -xvf backup.tar
## OUTPUT
<img width="1115" height="343" alt="image" src="https://github.com/user-attachments/assets/c8cd1491-2c5d-4f38-8ff1-149ca03d7a5c" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="1115" height="95" alt="image" src="https://github.com/user-attachments/assets/872a8fcd-6141-4789-bcf9-71c9ae037901" />

gunzip backup.tar.gz
## OUTPUT
<img width="1115" height="99" alt="image" src="https://github.com/user-attachments/assets/a10e0792-0f94-4a8d-a308-af507d78b0f0" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="973" height="138" alt="image" src="https://github.com/user-attachments/assets/8941f2d2-7f58-447a-9d69-10ec8afc84ed" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="970" height="205" alt="image" src="https://github.com/user-attachments/assets/2a281e56-20ba-4909-bd78-9702a26b51ef" />


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
<img width="977" height="542" alt="image" src="https://github.com/user-attachments/assets/420bb1db-dd0d-45d7-b2f7-42fbdea734f0" />

 
ls file1
## OUTPUT
<img width="966" height="96" alt="image" src="https://github.com/user-attachments/assets/6ed9828c-92e9-4365-b77e-69ceaad7b30b" />

echo $?
## OUTPUT 
<img width="975" height="103" alt="image" src="https://github.com/user-attachments/assets/2edabeec-8172-4be9-8dbb-d320b8fb5223" />


./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="1022" height="105" alt="image" src="https://github.com/user-attachments/assets/74c7e369-907f-4618-b90b-6193b963f64c" />

abcd

 
echo $?
 ## OUTPUT
<img width="1022" height="105" alt="image" src="https://github.com/user-attachments/assets/be1cf33b-762e-4ec2-97cd-b761385ef26a" />


 
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
<img width="972" height="369" alt="image" src="https://github.com/user-attachments/assets/6508ad32-6d3b-4efb-9f97-289ffd17d3f1" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="971" height="91" alt="image" src="https://github.com/user-attachments/assets/86682835-19c5-4e0b-9f52-2f098a0380b4" />


# check file ownership
cat > psswdperm.sh 
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
<img width="975" height="105" alt="image" src="https://github.com/user-attachments/assets/9089b95a-132a-4cfb-aff4-3e71688db9b2" />


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

./ifnested.sh 
## OUTPUT
<img width="978" height="176" alt="image" src="https://github.com/user-attachments/assets/772db86c-edb9-462c-bb27-a7bd87b45785" />



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
<img width="970" height="143" alt="image" src="https://github.com/user-attachments/assets/82c829e0-4b76-4d6e-9f5a-f8b300e29adb" />

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
<img width="982" height="174" alt="image" src="https://github.com/user-attachments/assets/1cf31aa4-f30e-4ef3-bdd7-c9e425127ab7" />

# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = kabe ]
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
<img width="970" height="138" alt="image" src="https://github.com/user-attachments/assets/330862b7-9191-479c-b46c-e6f5952346c5" />


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
<img width="973" height="105" alt="image" src="https://github.com/user-attachments/assets/06c4f1e7-ecf0-4f3f-beeb-229c4c5cb955" />

# using the case command
cat >casecheck.sh 
```bash
case $USER in
kabe | Kabe)
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

<img width="972" height="135" alt="image" src="https://github.com/user-attachments/assets/75100dd6-c7d7-48ed-837f-fdaa5cb6d28b" />

cat > whiletest.sh
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
<img width="975" height="413" alt="image" src="https://github.com/user-attachments/assets/049ee34f-2037-420e-8fb3-20f6bdf652a5" />


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
 
 ./utiltest.sh
 ## Output
<img width="967" height="210" alt="image" src="https://github.com/user-attachments/assets/4d0e109f-679c-4d81-812b-ad3603b3b7d2" />

 
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
 
./forin1.sh

## Output
<img width="972" height="274" alt="image" src="https://github.com/user-attachments/assets/63083610-14ee-425b-8f80-055d17758707" />


cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
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

## Output
<img width="978" height="172" alt="image" src="https://github.com/user-attachments/assets/65f09d62-a418-44df-ba4f-f1d16d17f069" />

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

## Output
<img width="985" height="276" alt="image" src="https://github.com/user-attachments/assets/554d1da6-234a-44e5-b24b-0038481dd1d9" />


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
<img width="986" height="308" alt="image" src="https://github.com/user-attachments/assets/c19d3a3a-c52d-40d0-9d5e-7661145c2ad0" />


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
<img width="977" height="236" alt="image" src="https://github.com/user-attachments/assets/cbee294e-0ff0-4de2-8dcc-368a16332051" />

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
<img width="980" height="240" alt="image" src="https://github.com/user-attachments/assets/e1b4574e-4b9a-44e5-bde0-0494b180352a" />

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
<img width="977" height="473" alt="image" src="https://github.com/user-attachments/assets/7feef3ce-3623-4fbd-a2ae-2a4b511d63d7" />

 
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

## Output
<img width="982" height="176" alt="image" src="https://github.com/user-attachments/assets/55654fc7-2be8-4bce-9993-e1d86ff26142" />

 
cat forcontinue.sh 
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
<img width="977" height="236" alt="image" src="https://github.com/user-attachments/assets/41feda07-546b-4885-a7af-808802487583" />

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
<img width="982" height="136" alt="image" src="https://github.com/user-attachments/assets/ecd3324f-ea6e-4e12-a966-6f0b66961f90" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

$ ./exread1.sh

## OUTPUT
<img width="982" height="135" alt="image" src="https://github.com/user-attachments/assets/17f31ce7-08c1-4f4a-ac6d-5774a9f8c263" />


 
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
<img width="972" height="104" alt="image" src="https://github.com/user-attachments/assets/b22b3780-af46-432d-810c-9ef64d0dca4c" />

 
 ./funcex.sh 1 2

<img width="976" height="99" alt="image" src="https://github.com/user-attachments/assets/147f1183-bc07-4f2c-bc63-aed60682030b" />

 
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

<img width="986" height="174" alt="image" src="https://github.com/user-attachments/assets/963554ec-ced9-423a-8d2c-9313d03cd95a" />


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
$ chmod 777 argshift1.sh
## OUTPUT
$ ./argshift1.sh 1 2 3

<img width="974" height="174" alt="image" src="https://github.com/user-attachments/assets/0bcac45e-a26c-4a71-b143-bc2e429004d6" />


cat > argshift.sh
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
 ./argshift.sh 1 2 3

 <img width="973" height="549" alt="image" src="https://github.com/user-attachments/assets/72f3f352-91a0-4a3d-9022-c699ca39ec1c" />

 
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

<img width="972" height="513" alt="image" src="https://github.com/user-attachments/assets/c42dc19c-cac1-4404-a717-64bbe97f587f" />

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

<img width="988" height="339" alt="image" src="https://github.com/user-attachments/assets/20169740-daba-4b46-aba7-e997248f438f" />


# RESULT:
The Commands are executed successfully.
