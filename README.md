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
<img width="253" height="154" alt="image" src="https://github.com/user-attachments/assets/12dff9db-d78d-48d4-86b6-8763ce748884" />



cat < file2
## OUTPUT
<img width="287" height="169" alt="image" src="https://github.com/user-attachments/assets/5f89b410-1c96-4ed2-8bbb-00cbebb22648" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="360" height="75" alt="image" src="https://github.com/user-attachments/assets/7cc12ea3-bdf9-4aa9-8d67-97eff7d7dda0" />

comm file1 file2
 ## OUTPUT
<img width="310" height="220" alt="image" src="https://github.com/user-attachments/assets/c38e9c37-ad96-4f85-b922-f89c75d657f2" />

 
diff file1 file2
## OUTPUT
<img width="296" height="268" alt="image" src="https://github.com/user-attachments/assets/fe216447-7f0c-4664-bb70-062b6a59dbfe" />



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
<img width="276" height="107" alt="image" src="https://github.com/user-attachments/assets/59305e0b-ac0a-4678-bbdd-efa2cbe562ee" />





cut -d "|" -f 1 file22
## OUTPUT




cut -d "|" -f 2 file22
## OUTPUT
<img width="553" height="78" alt="image" src="https://github.com/user-attachments/assets/2f555914-f970-41ab-b821-bf97714f62a7" />


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
<img width="262" height="74" alt="image" src="https://github.com/user-attachments/assets/94dd024b-402e-4d94-9d6e-a7948b2b8631" />




grep hello newfile 
## OUTPUT
<img width="262" height="74" alt="image" src="https://github.com/user-attachments/assets/37d422db-c735-4350-9c66-716ae0e7d723" />





grep -v hello newfile 
## OUTPUT
<img width="303" height="83" alt="image" src="https://github.com/user-attachments/assets/bcbd0057-aeb8-4384-9e2d-90a45fa87a65" />




cat newfile | grep -i "hello"
## OUTPUT
<img width="410" height="98" alt="image" src="https://github.com/user-attachments/assets/4e8ca092-097a-4e4e-b826-fb913dcceefc" />





cat newfile | grep -i -c "hello"
## OUTPUT
<img width="401" height="70" alt="image" src="https://github.com/user-attachments/assets/6bc0355e-3a05-42e5-8804-45bc3fe0d4f5" />





grep -R ubuntu /etc
## OUTPUT
<img width="377" height="99" alt="image" src="https://github.com/user-attachments/assets/f6be4906-3e69-48f9-82e7-4524f3635f96" />



grep -w -n world newfile   
## OUTPUT
<img width="1522" height="662" alt="image" src="https://github.com/user-attachments/assets/1bc5ad41-c3be-47fc-8fef-455391a16dcb" />


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
<img width="398" height="95" alt="image" src="https://github.com/user-attachments/assets/37efdb44-849d-4a81-9755-7fbf212be4bd" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="398" height="95" alt="image" src="https://github.com/user-attachments/assets/09eb1432-d632-4446-8fa1-8fc1b361dccd" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="407" height="94" alt="image" src="https://github.com/user-attachments/assets/32e8f978-f0d0-48b2-96ea-252e6d556ca8" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="327" height="77" alt="image" src="https://github.com/user-attachments/assets/3e0ed037-94a7-4f4f-93f8-6b90fc19baca" />



egrep '(world$)' newfile 
## OUTPUT
<img width="352" height="96" alt="image" src="https://github.com/user-attachments/assets/a8dcd323-c626-4169-b9ff-2b81c3a9c493" />



egrep '(World$)' newfile 
## OUTPUT
<img width="352" height="96" alt="image" src="https://github.com/user-attachments/assets/2d10debc-a151-46d7-b87e-3687241e9ae8" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="368" height="126" alt="image" src="https://github.com/user-attachments/assets/73a5a736-5c08-4bc1-a3f1-da2d92b0bf62" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="319" height="67" alt="image" src="https://github.com/user-attachments/assets/74e78aea-2376-4a74-97d1-187be27be911" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="383" height="78" alt="image" src="https://github.com/user-attachments/assets/f5a41b2d-d116-43e5-b647-df0e8aed4a92" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="372" height="65" alt="image" src="https://github.com/user-attachments/assets/808e7c2d-5c05-43a3-b599-06ff83d52110" />


egrep l{2} newfile
## OUTPUT
<img width="273" height="104" alt="image" src="https://github.com/user-attachments/assets/d98fb183-669f-47a5-802a-2397a7ee8190" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="352" height="376" alt="image" src="https://github.com/user-attachments/assets/1b2559e7-1aca-4964-a5a8-bf3c0f82e9bc" />


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
<img width="342" height="81" alt="image" src="https://github.com/user-attachments/assets/eee80449-1310-4ea4-b9c8-b83542dea6b2" />



sed -n -e '$p' file23
## OUTPUT
<img width="335" height="78" alt="image" src="https://github.com/user-attachments/assets/35caf44b-9edc-491a-a90b-f65103764488" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="432" height="256" alt="image" src="https://github.com/user-attachments/assets/ddec11d6-d4e7-4740-acc7-2e75a69a7f6c" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="407" height="255" alt="image" src="https://github.com/user-attachments/assets/84f7a03a-4554-4f12-b498-f503bb3519b0" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="425" height="250" alt="image" src="https://github.com/user-attachments/assets/316d8948-49a0-4e66-bb04-95d7e424e744" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="368" height="178" alt="image" src="https://github.com/user-attachments/assets/ee77c79e-7059-4e64-8144-80297243b0ed" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="403" height="120" alt="image" src="https://github.com/user-attachments/assets/26cca0dd-3069-4bb3-83e8-393096f6ab1f" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="398" height="95" alt="image" src="https://github.com/user-attachments/assets/c3581631-06ec-4dba-b5d0-fddd6b235afc" />



seq 10 
## OUTPUT
<img width="377" height="305" alt="image" src="https://github.com/user-attachments/assets/54f6ffa0-ef8d-47ee-a4d5-40a642fc0368" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="337" height="124" alt="image" src="https://github.com/user-attachments/assets/38228ff0-37ac-443d-b8a1-c161257539c9" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="377" height="126" alt="image" src="https://github.com/user-attachments/assets/c5e1b5d8-93ee-4ff3-bddf-f323a1650711" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="392" height="149" alt="image" src="https://github.com/user-attachments/assets/eadb443d-d520-4651-aa0f-40dc111e3477" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="367" height="131" alt="image" src="https://github.com/user-attachments/assets/b75be265-2d89-4e77-aaa5-1417cd367948" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="392" height="125" alt="image" src="https://github.com/user-attachments/assets/de1dc553-ee08-4d8c-8ada-e13a1fdccf84" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="343" height="201" alt="image" src="https://github.com/user-attachments/assets/d6204788-40ab-4035-8653-ba69168a8b9a" />




sed -n '2,4{s/$/*/;p}' file23
<img width="431" height="127" alt="image" src="https://github.com/user-attachments/assets/87d6d3c0-ded1-4e78-8805-69aea7e26eab" />


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
<img width="398" height="128" alt="image" src="https://github.com/user-attachments/assets/7f5a02ef-612f-483f-9ff3-463474a8a367" />


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
<img width="492" height="221" alt="image" src="https://github.com/user-attachments/assets/c7e1924d-e5df-4087-bb85-8071132499b2" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="452" height="245" alt="image" src="https://github.com/user-attachments/assets/9dffcab9-a729-4c61-8f44-f692e17e779e" />

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
<img width="487" height="129" alt="image" src="https://github.com/user-attachments/assets/0a3bb5cf-ede7-4f4c-95dd-d3c3d1ee8e27" />



 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="411" height="130" alt="image" src="https://github.com/user-attachments/assets/6d8d94e4-1086-4365-880c-bc7d9800305c" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT


tar -xvf backup.tar
## OUTPUT

gzip backup.tar

ls .gz
## OUTPUT
<img width="802" height="874" alt="image" src="https://github.com/user-attachments/assets/117642ba-42d9-43cb-897e-ddf401cd22ba" />

gunzip backup.tar.gz
## OUTPUT
<img width="1053" height="85" alt="image" src="https://github.com/user-attachments/assets/f2e08c40-d85b-457b-979f-cb0366c81d1d" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="361" height="170" alt="image" src="https://github.com/user-attachments/assets/846cfc76-d2ae-4408-bf69-b109d0453b9c" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="361" height="170" alt="image" src="https://github.com/user-attachments/assets/cb5aef61-00e8-430e-9c10-b7870d3da434" />


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
<img width="335" height="31" alt="image" src="https://github.com/user-attachments/assets/9a8247f4-1059-489b-979c-53d74d91b053" />
<img width="461" height="377" alt="image" src="https://github.com/user-attachments/assets/d2793d1a-d779-463d-a49c-92626ee7ddfd" />
<img width="335" height="65" alt="image" src="https://github.com/user-attachments/assets/bf8a96b3-6366-49b1-a03b-4f5db21f9a13" />

 
ls file1
## OUTPUT
<img width="907" height="473" alt="image" src="https://github.com/user-attachments/assets/670ea63d-e31f-4740-9fa1-dd86bedcde92" />

echo $?
## OUTPUT 
<img width="218" height="66" alt="image" src="https://github.com/user-attachments/assets/3e340106-6554-45c5-9100-9191946afc19" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="307" height="79" alt="image" src="https://github.com/user-attachments/assets/a0066a94-1bdb-4951-be66-0f21ac39eb5d" />
 
abcd
 
echo $?
 ## OUTPUT
<img width="307" height="79" alt="image" src="https://github.com/user-attachments/assets/c9ec74b8-1a66-48e0-a80e-e37fc931f1c3" />


 
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
<img width="498" height="265" alt="image" src="https://github.com/user-attachments/assets/7ec1887b-315c-49e0-bd10-f510b02cc30c" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="745" height="102" alt="image" src="https://github.com/user-attachments/assets/ee5ed99c-7704-4cf5-9895-da7fc39fe646" />


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
<img width="773" height="245" alt="image" src="https://github.com/user-attachments/assets/dcfaa4cd-4a6d-497b-a32b-f2ba6decac9e" />
<img width="852" height="96" alt="image" src="https://github.com/user-attachments/assets/fd0c4696-b848-4764-9342-d2a8e41eb20b" />

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
<img width="633" height="563" alt="image" src="https://github.com/user-attachments/assets/e2ff9b1d-b01c-41ef-a009-9c8444e7c5cb" />
<img width="788" height="165" alt="image" src="https://github.com/user-attachments/assets/dacc3ea2-ff9b-4385-ac4f-be2d9cc921ac" />



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
<img width="617" height="442" alt="image" src="https://github.com/user-attachments/assets/8a246139-dd9b-47e8-93ba-2e7863467622" />
<img width="710" height="432" alt="image" src="https://github.com/user-attachments/assets/4f0ce1e5-0d84-44a6-ab00-05cc537c4183" />
<img width="747" height="133" alt="image" src="https://github.com/user-attachments/assets/bb44d502-a8b5-42d2-bb41-9304b6f4eb91" />

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
<img width="892" height="518" alt="image" src="https://github.com/user-attachments/assets/a2ce72ff-b3ae-4da6-afe9-c76da14430e4" />
<img width="747" height="147" alt="image" src="https://github.com/user-attachments/assets/112f349e-7366-4e47-8682-d94735b77b83" />


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
<img width="757" height="551" alt="image" src="https://github.com/user-attachments/assets/ec1ba0cf-0275-4ac0-b868-5d61b1c34779" />
<img width="828" height="93" alt="image" src="https://github.com/user-attachments/assets/7e469643-9d8c-4b80-a346-638718de5154" />


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
<img width="708" height="460" alt="image" src="https://github.com/user-attachments/assets/a7bfa609-c6a1-4275-9201-fc7455886ff1" />
<img width="806" height="97" alt="image" src="https://github.com/user-attachments/assets/ac30d881-87d4-4001-a6b8-05755ff6feaa" />
<img width="531" height="67" alt="image" src="https://github.com/user-attachments/assets/6fe18809-b7d1-4fe7-a2a5-8c0e56c5cbf9" />

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
<img width="425" height="32" alt="image" src="https://github.com/user-attachments/assets/ba48a2ce-8199-4ed2-b4fb-92507e72731b" />
<img width="563" height="67" alt="image" src="https://github.com/user-attachments/assets/e4f6f654-82cc-42c3-9acb-1f8f4203702b" />
<img width="747" height="380" alt="image" src="https://github.com/user-attachments/assets/7533c17f-9081-4b51-8f00-af030b5f4d73" />
<img width="438" height="60" alt="image" src="https://github.com/user-attachments/assets/3569c721-2a02-4872-a77d-822603c970c0" />

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
<img width="351" height="258" alt="image" src="https://github.com/user-attachments/assets/933ffafc-73dc-46f8-95e0-d79e5f1e9e35" />
<img width="707" height="190" alt="image" src="https://github.com/user-attachments/assets/0dd5b404-5b3f-4a62-88d0-c83ebe589db5" />

 
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
<img width="417" height="180" alt="image" src="https://github.com/user-attachments/assets/bfb652ae-26bc-4418-a149-368804e8ff33" />

 
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
 <img width="688" height="215" alt="image" src="https://github.com/user-attachments/assets/4250590f-cee6-4662-a202-3aae79a0dd55" />
<img width="927" height="193" alt="image" src="https://github.com/user-attachments/assets/0b796a1c-1c4a-48f6-9e4c-a8c21f888e25" />

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
<img width="776" height="291" alt="image" src="https://github.com/user-attachments/assets/e41080ac-62b1-4dfd-9b84-aaa6295f2aa3" />

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
<img width="737" height="218" alt="image" src="https://github.com/user-attachments/assets/7d7feee8-d44d-4daf-9012-377830cc2e38" />

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

<img width="433" height="202" alt="image" src="https://github.com/user-attachments/assets/2a39939a-a840-4024-a793-eb43326be30c" />

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
<img width="201" height="230" alt="image" src="https://github.com/user-attachments/assets/86a2fdea-10e2-423d-8ca5-4fa5ca1c3504" />


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
<img width="317" height="187" alt="image" src="https://github.com/user-attachments/assets/38c3fff8-c076-460e-82cf-87cfc9817304" />


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
<img width="402" height="183" alt="image" src="https://github.com/user-attachments/assets/ed137855-e8b9-4092-b1cf-e879c83f6660" />

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
<img width="382" height="410" alt="image" src="https://github.com/user-attachments/assets/3d3ee398-6e3e-418b-8902-2348f344b766" />

 
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
<img width="297" height="97" alt="image" src="https://github.com/user-attachments/assets/028e2c57-a858-479c-834f-7e82eae69d10" />

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
 <img width="332" height="165" alt="image" src="https://github.com/user-attachments/assets/f99355af-f143-4d12-a9f1-abd33c9477ce" />

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
<img width="315" height="60" alt="image" src="https://github.com/user-attachments/assets/350d698b-5a36-490f-8fd3-551df6ab91aa" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="315" height="60" alt="image" src="https://github.com/user-attachments/assets/9b598042-6763-4541-9109-cdd72d448c17" />



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
<img width="315" height="60" alt="image" src="https://github.com/user-attachments/assets/08822362-b255-4790-a92a-4bb0920d9460" />

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
<img width="315" height="60" alt="image" src="https://github.com/user-attachments/assets/8cd23b1f-a81c-4f6d-8ea2-ef2756ce5ffe" />


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

<img width="378" height="120" alt="image" src="https://github.com/user-attachments/assets/86a1b6c1-8b83-47bc-8e2f-5c834b9f822d" />

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
```
## OUTPUT

<img width="597" height="470" alt="image" src="https://github.com/user-attachments/assets/f25ad1c1-cff3-4856-b1a5-ccf2a5dc6240" />

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
<img width="435" height="440" alt="image" src="https://github.com/user-attachments/assets/9b167eaf-5632-4857-a610-690aaa0585fb" />


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
<img width="820" height="811" alt="image" src="https://github.com/user-attachments/assets/083d73ab-e603-4b6f-9686-bd82da1beef3" />




# RESULT:
The Commands are executed successfully.
