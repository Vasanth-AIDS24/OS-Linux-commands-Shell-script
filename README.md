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
<img width="962" height="256" alt="image" src="https://github.com/user-attachments/assets/aafbcdec-92cb-497b-af88-ed9644c9befc" />



cat < file2
## OUTPUT
<img width="943" height="301" alt="image" src="https://github.com/user-attachments/assets/acf1de81-cd16-4dc9-b72a-9da39d16e3d5" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="961" height="116" alt="image" src="https://github.com/user-attachments/assets/b090d352-6ecf-41ea-898a-fa12a5dcdc7a" />

comm file1 file2
 ## OUTPUT
<img width="948" height="308" alt="image" src="https://github.com/user-attachments/assets/9a5a1f5e-5fac-411c-a307-841986f0a6ae" />

 
diff file1 file2
## OUTPUT
<img width="527" height="181" alt="image" src="https://github.com/user-attachments/assets/7f48e2fd-daa7-4cdc-9d82-94af40e5c740" />


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
<img width="527" height="58" alt="image" src="https://github.com/user-attachments/assets/73d27c26-c4b7-4164-b898-60552b0227d2" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="553" height="78" alt="image" src="https://github.com/user-attachments/assets/a19bdf8c-c07d-47a8-8392-5042cdbb658b" />



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
<img width="553" height="42" alt="image" src="https://github.com/user-attachments/assets/9985e063-beda-4578-9ae0-c40e116d081a" />



grep hello newfile 
## OUTPUT
<img width="553" height="42" alt="image" src="https://github.com/user-attachments/assets/b7fd77f3-7fbc-44ba-bc10-d05fea58d641" />




grep -v hello newfile 
## OUTPUT
<img width="553" height="42" alt="image" src="https://github.com/user-attachments/assets/7cb15b41-ef6f-4d9a-ad97-fc39a0946444" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="613" height="63" alt="image" src="https://github.com/user-attachments/assets/cc6985e9-0cea-40d0-9ce7-0155ed870b57" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="643" height="39" alt="image" src="https://github.com/user-attachments/assets/c860c63d-4f9d-4000-8bd5-07d2322a25d5" />




grep -R ubuntu /etc
## OUTPUT
<img width="920" height="326" alt="image" src="https://github.com/user-attachments/assets/d3fedfe7-83d5-4db2-afd5-d933f4c3eb57" />



grep -w -n world newfile   
## OUTPUT
<img width="610" height="57" alt="image" src="https://github.com/user-attachments/assets/18480c76-4b8c-49c6-9add-283032198d50" />


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
<img width="627" height="63" alt="image" src="https://github.com/user-attachments/assets/fa817802-ee3b-4454-a2be-c70ab9100242" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="643" height="60" alt="image" src="https://github.com/user-attachments/assets/bca11d08-9399-4683-b43c-ae6a13d6bfdb" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="643" height="60" alt="image" src="https://github.com/user-attachments/assets/3f9636be-3330-4640-b786-b1d264510209" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="643" height="47" alt="image" src="https://github.com/user-attachments/assets/0b4b0fdd-ef56-4ef4-931b-b6f3b2358c93" />



egrep '(world$)' newfile 
## OUTPUT
<img width="643" height="59" alt="image" src="https://github.com/user-attachments/assets/b8ba065c-849e-474a-b4d7-158d18a115ad" />



egrep '(World$)' newfile 
## OUTPUT
<img width="643" height="42" alt="image" src="https://github.com/user-attachments/assets/b016fe1f-374b-4c99-9816-80f3134e79a8" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="643" height="76" alt="image" src="https://github.com/user-attachments/assets/e5fb360d-cea0-424e-a834-8b2a75ce28eb" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="643" height="47" alt="image" src="https://github.com/user-attachments/assets/e7d512b9-d2cd-437c-90c9-bd9cfc1df4de" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="643" height="45" alt="image" src="https://github.com/user-attachments/assets/8364ec89-8ed5-4c6f-8962-91624255a2f3" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="643" height="45" alt="image" src="https://github.com/user-attachments/assets/3a349891-abaa-419c-bf56-16486e883578" />


egrep l{2} newfile
## OUTPUT
<img width="643" height="57" alt="image" src="https://github.com/user-attachments/assets/942fbaaf-850d-496a-8df7-c74b3f74c240" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="643" height="75" alt="image" src="https://github.com/user-attachments/assets/366b5d8c-90d2-4ab9-9281-af6142a724d3" />


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
<img width="643" height="46" alt="image" src="https://github.com/user-attachments/assets/0add7a8f-8c7b-47fe-8a26-f70b27624ed8" />



sed -n -e '$p' file23
## OUTPUT
<img width="643" height="39" alt="image" src="https://github.com/user-attachments/assets/b0761d9f-0fe2-4cd9-98ea-8901e40cba76" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="643" height="169" alt="image" src="https://github.com/user-attachments/assets/fcadae3b-2c5f-4720-af0d-82dc1283742b" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="643" height="169" alt="image" src="https://github.com/user-attachments/assets/e46125f3-a0f3-4df0-ba07-9eda29c9e3e7" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="643" height="169" alt="image" src="https://github.com/user-attachments/assets/dfc633ec-d314-4a00-bcb4-f25400c4a7f2" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="643" height="113" alt="image" src="https://github.com/user-attachments/assets/6e838d2d-9a8a-4a65-8ca4-49c3929fe641" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="643" height="77" alt="image" src="https://github.com/user-attachments/assets/72154bc2-f3ce-4260-9976-dae301bcb5d9" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="643" height="60" alt="image" src="https://github.com/user-attachments/assets/69cc3964-bf81-40a0-bed0-c1c6524b22f9" />



seq 10 
## OUTPUT
<img width="643" height="203" alt="image" src="https://github.com/user-attachments/assets/d059739c-ed51-43a5-9cf2-911a6aa18217" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="643" height="75" alt="image" src="https://github.com/user-attachments/assets/2840202f-d2d9-44e7-946f-5abe1490e7d4" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="643" height="75" alt="image" src="https://github.com/user-attachments/assets/d182ea4f-671a-4b80-96b8-4cde08ab2b25" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="643" height="94" alt="image" src="https://github.com/user-attachments/assets/332b28d5-a77a-4f9a-9395-050f9160fd1b" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="643" height="83" alt="image" src="https://github.com/user-attachments/assets/f57ca246-37bd-439b-bc43-244070172e32" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="643" height="80" alt="image" src="https://github.com/user-attachments/assets/1079a571-69a0-40e7-8207-24e5437c0a99" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="643" height="90" alt="image" src="https://github.com/user-attachments/assets/73798392-7b22-4b94-bc24-c3d736fe54d7" />
<img width="643" height="77" alt="image" src="https://github.com/user-attachments/assets/33b9dd65-02ba-492a-a2ab-42618bf079ba" />



sed -n '2,4{s/$/*/;p}' file23


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
<img width="643" height="93" alt="image" src="https://github.com/user-attachments/assets/d819f1ad-efd9-4178-b36a-98875fc408fc" />


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
<img width="643" height="115" alt="image" src="https://github.com/user-attachments/assets/a59cc85e-f4b4-4395-bf9f-e2f59e083c05" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="677" height="166" alt="image" src="https://github.com/user-attachments/assets/a0339471-b079-46ea-883c-0a2db53ee5f8" />

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
<img width="677" height="85" alt="image" src="https://github.com/user-attachments/assets/c16f05c5-50be-4160-b58c-44f54bc1b86e" />



 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="728" height="79" alt="image" src="https://github.com/user-attachments/assets/3eea857b-9973-4ded-b013-de1d1a9a8720" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="863" height="157" alt="image" src="https://github.com/user-attachments/assets/c07f3a27-f2d4-47eb-ad68-7f4e541f0a29" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="844" height="204" alt="image" src="https://github.com/user-attachments/assets/08f4754d-867e-4294-b827-275dc34d65e1" />


tar -xvf backup.tar
## OUTPUT
<img width="518" height="200" alt="image" src="https://github.com/user-attachments/assets/6ad35f44-2563-443d-a9c8-275bdc71e961" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="518" height="44" alt="image" src="https://github.com/user-attachments/assets/e11e1a82-3a73-466c-941c-0a3a41920b37" />

gunzip backup.tar.gz
## OUTPUT
<img width="704" height="308" alt="image" src="https://github.com/user-attachments/assets/607f4296-aa6c-4a76-984b-8c5fcc6f027f" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="529" height="48" alt="image" src="https://github.com/user-attachments/assets/1544943f-3677-4a6e-afff-83b18c42ad32" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="532" height="63" alt="image" src="https://github.com/user-attachments/assets/27979399-5c40-4ebb-ade2-8692f5024b29" />


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
<img width="571" height="345" alt="image" src="https://github.com/user-attachments/assets/e3287b27-fec6-4e5a-874a-7e5e1e481d10" />

 
ls file1
## OUTPUT
<img width="571" height="49" alt="image" src="https://github.com/user-attachments/assets/ec4872c5-6bc3-4207-9c25-ca70fe895bb9" />

echo $?
## OUTPUT 
<img width="571" height="43" alt="image" src="https://github.com/user-attachments/assets/27547a2e-e62b-4ef8-8aeb-a4df634d1b48" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="571" height="43" alt="image" src="https://github.com/user-attachments/assets/444b13be-8d4f-4030-8685-711a3a2f322c" />
 
abcd
 
echo $?
 ## OUTPUT
<img width="571" height="43" alt="image" src="https://github.com/user-attachments/assets/3d73ad78-490d-41dd-ac66-91277abfea24" />


 
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
<img width="571" height="62" alt="image" src="https://github.com/user-attachments/assets/6746ea54-b535-47ec-8a69-28d0f2c54d42" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="593" height="61" alt="image" src="https://github.com/user-attachments/assets/b3420bf0-8414-4c04-9faa-f55615703c1c" />


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
<img width="812" height="114" alt="image" src="https://github.com/user-attachments/assets/17fcc36e-8fe3-468e-b9f0-0a70a5805e64" />

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
<img width="812" height="114" alt="image" src="https://github.com/user-attachments/assets/cbadcdf4-ef3c-415f-baca-b4222b6c1882" />



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
<img width="812" height="114" alt="image" src="https://github.com/user-attachments/assets/510bcaee-94ca-471d-97e1-bca8f5ab15c7" />

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
<img width="812" height="114" alt="image" src="https://github.com/user-attachments/assets/d86bbf26-e2fb-4bd8-b999-93e4b17d4a7f" />


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
<img width="812" height="79" alt="image" src="https://github.com/user-attachments/assets/d762dbdc-165e-4159-82ce-c23f9b3c4839" />


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
<img width="812" height="79" alt="image" src="https://github.com/user-attachments/assets/84355389-3584-41e3-a843-270f2b34861d" />

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
 <img width="728" height="79" alt="image" src="https://github.com/user-attachments/assets/b0c1605f-bb33-4cf0-9b8f-b5be85861ae6" />

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
 <img width="595" height="133" alt="image" src="https://github.com/user-attachments/assets/40fd3dd1-902a-4155-8f41-07a2f8b3269f" />

 
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
 
 <img width="595" height="133" alt="image" src="https://github.com/user-attachments/assets/66ffffb6-d888-4137-9098-c7a9c90f9d2d" />

 
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
 <img width="595" height="167" alt="image" src="https://github.com/user-attachments/assets/c886c26e-3698-42fe-82d1-68d282735bb0" />

 
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
<img width="595" height="133" alt="image" src="https://github.com/user-attachments/assets/719621b7-1aa8-4f74-a4d5-cc1a584a2e1b" />

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

<img width="595" height="76" alt="image" src="https://github.com/user-attachments/assets/3315c34d-bfca-4800-aa2e-ea9b5d0d0037" />

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

<img width="595" height="291" alt="image" src="https://github.com/user-attachments/assets/c033f3eb-fa5e-43bf-b818-51f3d9f4049b" />

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

 <img width="559" height="281" alt="image" src="https://github.com/user-attachments/assets/116e6cb1-07b3-453a-bd89-de5a5a2b78a5" />

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

<img width="599" height="112" alt="image" src="https://github.com/user-attachments/assets/f5b2bcb5-740d-48c1-a2dd-53878042348a" />



# RESULT:
The Commands are executed successfully.
