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
<img width="427" height="118" alt="image" src="https://github.com/user-attachments/assets/5006f03d-8561-4d96-883c-b0ddc2df43d7" />



cat < file2
## OUTPUT
<img width="371" height="179" alt="image" src="https://github.com/user-attachments/assets/e681826a-8dec-4aba-9afe-374226f4cce0" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="550" height="349" alt="image" src="https://github.com/user-attachments/assets/aa79c66a-0673-40f2-89c7-970979908a4a" />

comm file1 file2
 ## OUTPUT
<img width="504" height="54" alt="image" src="https://github.com/user-attachments/assets/9a6daa34-a137-474e-979f-f6dbee40eaad" />

 
diff file1 file2
## OUTPUT
<img width="493" height="274" alt="image" src="https://github.com/user-attachments/assets/25209f1d-d917-4ee4-9297-cf8954dbf040" />


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
<img width="452" height="104" alt="image" src="https://github.com/user-attachments/assets/6efd9d49-2061-4857-9b4d-43825f585c3b" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="503" height="129" alt="image" src="https://github.com/user-attachments/assets/2003748d-bcef-4004-b292-0d6f914c02be" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="518" height="128" alt="image" src="https://github.com/user-attachments/assets/4113c521-96f7-4f29-8033-84affcaf9fb7" />


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
<img width="473" height="57" alt="image" src="https://github.com/user-attachments/assets/d52c8862-0e83-4050-a212-5fcc0dbf8ce6" />



grep hello newfile 
## OUTPUT
 <img width="485" height="57" alt="image" src="https://github.com/user-attachments/assets/001b3876-0130-41f3-99ba-0c05761cd97e" />




grep -v hello newfile 
## OUTPUT
<img width="506" height="65" alt="image" src="https://github.com/user-attachments/assets/c17065a8-2cd2-49a2-9ca4-31b755648c48" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="608" height="86" alt="image" src="https://github.com/user-attachments/assets/9b1465ce-560c-4a0e-aae7-ae4a3eb721cf" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="669" height="58" alt="image" src="https://github.com/user-attachments/assets/efc0c0e2-c641-43c9-98b4-4d47ce4d675a" />




grep -R ubuntu /etc
## OUTPUT
<img width="667" height="240" alt="image" src="https://github.com/user-attachments/assets/886c12b1-fe6b-4eac-bc07-42e6d55dcb88" />



grep -w -n world newfile   
## OUTPUT
<img width="567" height="87" alt="image" src="https://github.com/user-attachments/assets/43ae9fd6-2b38-489e-a5a5-73b0549f170c" />


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

<img width="655" height="88" alt="image" src="https://github.com/user-attachments/assets/610aed1b-f2c5-4c79-bca4-55b40c0a880e" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="615" height="91" alt="image" src="https://github.com/user-attachments/assets/d12ce54b-ca6f-47b4-b81a-ba0988e7b6e8" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="677" height="85" alt="image" src="https://github.com/user-attachments/assets/c41ace41-7e15-42c4-b58d-d10effb2a70e" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="579" height="60" alt="image" src="https://github.com/user-attachments/assets/56ffcade-0905-4e79-b086-25129d88724a" />



egrep '(world$)' newfile 
## OUTPUT
<img width="607" height="57" alt="image" src="https://github.com/user-attachments/assets/4f7c7213-931f-4fd3-9c93-3ddd57334244" />



egrep '(World$)' newfile 
## OUTPUT
<img width="562" height="62" alt="image" src="https://github.com/user-attachments/assets/ff233455-f84b-4b53-8101-3117ffc05868" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="608" height="85" alt="image" src="https://github.com/user-attachments/assets/c9933bc8-870d-40c5-ab6a-e821fdd60b52" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="516" height="64" alt="image" src="https://github.com/user-attachments/assets/414bc258-5c96-4b83-9b44-7ed736353049" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="628" height="61" alt="image" src="https://github.com/user-attachments/assets/aaf0d1c3-3789-4b07-9c4b-670b07909243" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="606" height="68" alt="image" src="https://github.com/user-attachments/assets/44eff8df-f417-4d1a-8d2f-697f26ab7cee" />


egrep l{2} newfile
## OUTPUT

<img width="482" height="87" alt="image" src="https://github.com/user-attachments/assets/5ff87364-e993-4869-8b0b-f5d979dee0ce" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="528" height="126" alt="image" src="https://github.com/user-attachments/assets/c6495d04-5e1c-43bc-a60a-79a375548c7d" />


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
<img width="500" height="56" alt="image" src="https://github.com/user-attachments/assets/fcda8136-f476-47fc-8737-f5e8b53f8ffb" />



sed -n -e '$p' file23
## OUTPUT

<img width="502" height="56" alt="image" src="https://github.com/user-attachments/assets/f3b94da6-c228-4829-9128-e16b4b34a4bc" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="574" height="265" alt="image" src="https://github.com/user-attachments/assets/083ae268-fa50-4a63-9658-97d66e8eb2d7" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="597" height="277" alt="image" src="https://github.com/user-attachments/assets/e8eccf6e-224e-43ef-8636-d3664614b47a" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="650" height="279" alt="image" src="https://github.com/user-attachments/assets/e1bc6651-9c8b-4aa5-a3ca-e85c73fdc406" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="529" height="182" alt="image" src="https://github.com/user-attachments/assets/8e42beba-516f-4c53-9e03-55ca69dcc5d1" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="596" height="117" alt="image" src="https://github.com/user-attachments/assets/85af083c-cddb-442e-9a58-810f749d6816" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="640" height="88" alt="image" src="https://github.com/user-attachments/assets/4f48dc58-9ab1-4b10-9e53-1ddca380e373" />



seq 10 
## OUTPUT
<img width="479" height="336" alt="image" src="https://github.com/user-attachments/assets/d764a6b6-00e2-43e5-af21-502c21e0daf5" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="574" height="116" alt="image" src="https://github.com/user-attachments/assets/d2873545-8fc2-4993-9bf6-15572b263a23" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="540" height="116" alt="image" src="https://github.com/user-attachments/assets/d500fe17-d89b-4e83-b991-16639688d8dc" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="556" height="124" alt="image" src="https://github.com/user-attachments/assets/3a8cf0b2-115f-4647-b8aa-4b9484453bbe" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="523" height="145" alt="image" src="https://github.com/user-attachments/assets/5d08c53f-1868-48e4-9fee-419dc8096ca1" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="572" height="122" alt="image" src="https://github.com/user-attachments/assets/5e170a7f-1c9b-4b03-8c9e-2400a2c811c5" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="623" height="115" alt="image" src="https://github.com/user-attachments/assets/3e529d5b-1e63-4ba4-9b1e-77057d308525" />



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
<img width="347" height="189" alt="image" src="https://github.com/user-attachments/assets/5c74d546-4960-4ea9-836b-3a40c79ece10" />


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
<img width="357" height="173" alt="image" src="https://github.com/user-attachments/assets/961b49af-037b-4928-9dbb-0516c4772768" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="705" height="264" alt="image" src="https://github.com/user-attachments/assets/323ea1c5-8627-4402-bf16-64730e457132" />

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
<img width="599" height="120" alt="image" src="https://github.com/user-attachments/assets/f3c906f7-ba52-4011-87d4-dd3e2fb2f2d3" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="746" height="126" alt="image" src="https://github.com/user-attachments/assets/5f38d9cf-5320-4ec9-9eff-ec48c83739c5" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="192" height="87" alt="image" src="https://github.com/user-attachments/assets/8824b75b-7249-4c99-891f-2475fb4db739" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="198" height="88" alt="image" src="https://github.com/user-attachments/assets/ef658681-11e2-4281-b353-979bc39f6905" />


tar -xvf backup.tar
## OUTPUT
<img width="223" height="87" alt="image" src="https://github.com/user-attachments/assets/eda1e1b2-00d3-461e-83e2-a9a9e5a86ac0" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="760" height="156" alt="image" src="https://github.com/user-attachments/assets/17fde4c9-820b-4349-a305-04dc1d2b5173" />

gunzip backup.tar.gz
## OUTPUT
<img width="763" height="225" alt="image" src="https://github.com/user-attachments/assets/f8fa2a32-d065-41ef-9103-ce97c4939d0c" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="767" height="319" alt="image" src="https://github.com/user-attachments/assets/91a05bdd-4d19-4c3f-b14a-f8616c509f57" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="452" height="122" alt="image" src="https://github.com/user-attachments/assets/e7957827-211d-4175-b59e-320b83300a4d" />


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
<img width="562" height="431" alt="image" src="https://github.com/user-attachments/assets/91ffa176-0b61-4d2d-8c31-2200c780e7fa" />

 
ls file1
## OUTPUT
<img width="327" height="60" alt="image" src="https://github.com/user-attachments/assets/a5101b9e-acf8-49ae-b3d9-3c3e7f993f1c" />

echo $?
## OUTPUT 
<img width="327" height="56" alt="image" src="https://github.com/user-attachments/assets/8cf08d05-696a-4839-be7c-931af9a23628" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="330" height="66" alt="image" src="https://github.com/user-attachments/assets/01aa5414-c38b-4d4d-a8b1-014bfad80716" />

abcd
 
echo $?
 ## OUTPUT
<img width="601" height="300" alt="image" src="https://github.com/user-attachments/assets/83f565c0-01e9-4129-8487-71c4f0a140b4" />


 
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
<img width="590" height="331" alt="image" src="https://github.com/user-attachments/assets/0f0c521a-45e2-4379-bece-8b9daf86d17b" />


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
<img width="780" height="314" alt="image" src="https://github.com/user-attachments/assets/64c1f04e-ed98-4cca-9147-5cf1b13eea12" />

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
<img width="658" height="534" alt="image" src="https://github.com/user-attachments/assets/e3cffddf-ccd1-4019-a75e-fe616e720f65" />



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
<img width="733" height="654" alt="image" src="https://github.com/user-attachments/assets/767fae4a-d7e9-4a0b-99cb-46ed45165b23" />


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
<img width="682" height="338" alt="image" src="https://github.com/user-attachments/assets/20b5d3a8-e9a8-4884-b2ae-86f67e2bc927" />

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
<img width="589" height="212" alt="image" src="https://github.com/user-attachments/assets/fb6269e8-9fa0-4288-a0d2-192917f6a470" />

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
<img width="533" height="276" alt="image" src="https://github.com/user-attachments/assets/c145403c-7758-43f2-8849-8e9725d276c6" />


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
<img width="505" height="272" alt="image" src="https://github.com/user-attachments/assets/29c3e9a7-60be-4340-a233-7424840aa26e" />

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
<img width="769" height="299" alt="image" src="https://github.com/user-attachments/assets/03edb8a5-1982-4d62-9608-3f74fe3858e1" />

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
<img width="774" height="293" alt="image" src="https://github.com/user-attachments/assets/dc76f4c5-8669-47f8-b4b1-3b796b3f2609" />

 
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
<img width="780" height="294" alt="image" src="https://github.com/user-attachments/assets/b680e69e-f5fd-4341-ab99-ac8beb8b3034" />

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
 <img width="403" height="304" alt="image" src="https://github.com/user-attachments/assets/6a5d6fdb-7fcb-4a76-8eaa-823c0fd9ce58" />

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
<img width="597" height="184" alt="image" src="https://github.com/user-attachments/assets/c3784d44-a59d-45b9-9eb8-796931ee5101" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="639" height="146" alt="image" src="https://github.com/user-attachments/assets/1c13a2f7-cdb0-4e9b-a20a-3ceea6778b57" />



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

 ./funcex.sh <img width="465" height="18" alt="image" src="https://github.com/user-attachments/assets/bb09e36a-33b9-4892-aabe-ffff5b49764e" />


 
 ./funcex.sh 1 2<img width="250" height="24" alt="image" src="https://github.com/user-attachments/assets/0a6699b8-748c-48ec-a4ed-fa4eb5551a57" />


 
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
<img width="125" height="61" alt="image" src="https://github.com/user-attachments/assets/a5bebce2-06c8-4193-ab08-92da01c213d4" />

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
<img width="61" height="71" alt="image" src="https://github.com/user-attachments/assets/cd1d8b9a-77ee-4cfa-a88e-289b12e203ba" />

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
<img width="223" height="375" alt="image" src="https://github.com/user-attachments/assets/1fdf69e4-a90d-452c-b4a2-433fc8193817" />

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
 <img width="246" height="246" alt="image" src="https://github.com/user-attachments/assets/001b1ab9-9f5d-4a19-894f-ba8f9dae08df" />

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


# RESULT:
The Commands are executed successfully.
