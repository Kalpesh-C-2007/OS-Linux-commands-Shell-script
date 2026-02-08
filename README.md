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
<img width="416" height="126" alt="Screenshot 2026-02-08 230516" src="https://github.com/user-attachments/assets/a51576cc-fa41-4b3c-ba10-bdc7b066abef" />



cat < file2
## OUTPUT
<img width="406" height="197" alt="image" src="https://github.com/user-attachments/assets/5f724ea3-3f40-4481-8574-975e9c641c3a" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="447" height="50" alt="image" src="https://github.com/user-attachments/assets/ec2d240d-bae4-4ca3-a40f-0cfda3210f3b" />

comm file1 file2
 ## OUTPUT
<img width="454" height="249" alt="image" src="https://github.com/user-attachments/assets/bab5d04e-ce01-4bbf-8b9a-c7a1ebd28fd5" />

 
diff file1 file2
## OUTPUT
<img width="524" height="381" alt="image" src="https://github.com/user-attachments/assets/17e6c975-0886-4a0c-8e37-75d746605c90" />


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

<img width="466" height="95" alt="image" src="https://github.com/user-attachments/assets/4c6898d1-3842-4df4-9514-edebc7c8860d" />



cut -d "|" -f 1 file22
## OUTPUT
<img width="538" height="130" alt="image" src="https://github.com/user-attachments/assets/bd4145c4-dc0c-4699-b690-46503c90b9f8" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="545" height="132" alt="image" src="https://github.com/user-attachments/assets/7946be3a-d177-4eef-be5e-5f698e016819" />


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
<img width="497" height="67" alt="image" src="https://github.com/user-attachments/assets/8728be3c-c5b7-447d-b263-d40e0f2ebe12" />



grep hello newfile 
## OUTPUT

<img width="497" height="67" alt="image" src="https://github.com/user-attachments/assets/2d3b4d62-8e9e-491b-b067-2ac89e2970de" />



grep -v hello newfile 
## OUTPUT
<img width="536" height="67" alt="image" src="https://github.com/user-attachments/assets/f0ae8839-556d-4ae4-a98f-b425dd8c148e" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="675" height="94" alt="image" src="https://github.com/user-attachments/assets/64fd08a9-5729-4589-8731-c812605eea67" />




cat newfile | grep -i -c "hello"
## OUTPUT

<img width="713" height="64" alt="image" src="https://github.com/user-attachments/assets/0dd84a90-149d-445c-bb1d-4176f9c02900" />



grep -R ubuntu /etc
## OUTPUT
<img width="753" height="268" alt="image" src="https://github.com/user-attachments/assets/7264f382-7625-4eec-a656-e4965ed734c8" />



grep -w -n world newfile   
## OUTPUT
<img width="580" height="93" alt="image" src="https://github.com/user-attachments/assets/dc793011-0cba-4f7d-84e9-e3804740977b" />


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
<img width="692" height="97" alt="image" src="https://github.com/user-attachments/assets/25aee516-7411-40c8-aaef-31e66c77b540" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="724" height="99" alt="image" src="https://github.com/user-attachments/assets/f6188a47-86dc-4fde-998a-fc34e8631528" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="734" height="100" alt="image" src="https://github.com/user-attachments/assets/6d3e554b-c2ad-4f63-b2ed-13c3752eed2e" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="591" height="65" alt="image" src="https://github.com/user-attachments/assets/8bcf03a1-d1a1-4da4-bd2c-36d21beb23c2" />



egrep '(world$)' newfile 
## OUTPUT
<img width="609" height="69" alt="image" src="https://github.com/user-attachments/assets/e26acf62-6705-4e1a-968e-07f8ddd992c6" />



egrep '(World$)' newfile 
## OUTPUT
<img width="590" height="61" alt="image" src="https://github.com/user-attachments/assets/4e6a2688-d4ad-487f-9a01-a6608bbfdc00" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="674" height="95" alt="image" src="https://github.com/user-attachments/assets/a2392242-dec8-4f99-822a-01cadc638ee6" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="557" height="76" alt="image" src="https://github.com/user-attachments/assets/e2812fa7-1249-4d5b-94be-7ec857a66fdd" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="661" height="67" alt="image" src="https://github.com/user-attachments/assets/6d074a05-b241-4e25-a06b-98a4d0edb406" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="666" height="70" alt="image" src="https://github.com/user-attachments/assets/3418ebd5-2df3-4dbf-8532-37400b8b7571" />


egrep l{2} newfile
## OUTPUT
<img width="644" height="87" alt="image" src="https://github.com/user-attachments/assets/8bf36f33-f110-409b-b35e-49edcde1f26b" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="592" height="140" alt="image" src="https://github.com/user-attachments/assets/9a72e6b9-4204-435b-a27e-fb9c2da9b4eb" />


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
<img width="543" height="60" alt="image" src="https://github.com/user-attachments/assets/73b913f5-7447-4716-b61e-aaaff6e8b174" />



sed -n -e '$p' file23
## OUTPUT
<img width="561" height="71" alt="image" src="https://github.com/user-attachments/assets/e399f497-6345-4e00-8234-50fd8ed3c17e" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="644" height="303" alt="image" src="https://github.com/user-attachments/assets/540a89e5-9271-4702-b97a-566a98b3ee26" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="647" height="299" alt="image" src="https://github.com/user-attachments/assets/3fd2c3a0-cbb2-40ec-93a8-b89ddb32b1a4" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="690" height="306" alt="Screenshot 2026-02-08 233037" src="https://github.com/user-attachments/assets/43e57e6e-7154-41a4-a02f-ebb26a12e3c2" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="598" height="207" alt="image" src="https://github.com/user-attachments/assets/0d90e70b-b636-422c-94cc-ff670acc4e95" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="640" height="136" alt="image" src="https://github.com/user-attachments/assets/0aa1631d-1350-4a6c-8a7b-51e635fb798a" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="694" height="103" alt="image" src="https://github.com/user-attachments/assets/8a99c30f-a069-4c76-9586-2cf6ac9cb80e" />


seq 10 
## OUTPUT

<img width="530" height="298" alt="image" src="https://github.com/user-attachments/assets/0667461e-97fa-4abc-95b0-a954a7326131" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="546" height="112" alt="image" src="https://github.com/user-attachments/assets/8a5260dc-bb19-4519-b882-6c21028aa2eb" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="578" height="110" alt="image" src="https://github.com/user-attachments/assets/b237886b-386a-4083-bc2b-669385c61e0c" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="554" height="136" alt="image" src="https://github.com/user-attachments/assets/48c561ab-a368-4a18-a18c-ed842c53f4f6" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="534" height="114" alt="image" src="https://github.com/user-attachments/assets/cfff262f-8c16-429a-8caa-3143b0d7e736" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="514" height="116" alt="image" src="https://github.com/user-attachments/assets/2e7a4103-5f0a-4285-b14c-7bce95ecad14" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="663" height="128" alt="image" src="https://github.com/user-attachments/assets/caa633a5-0db2-4f5f-a058-e5b56dc0d9c8" />


sed -n '2,4{s/$/*/;p}' file23

## OUTPUT
<img width="675" height="137" alt="image" src="https://github.com/user-attachments/assets/15de40e4-2454-49eb-9e25-395c950d7ce8" />



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
<img width="428" height="196" alt="image" src="https://github.com/user-attachments/assets/75d744ae-ab38-40c5-b748-4a19174fce1f" />


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
<img width="450" height="199" alt="image" src="https://github.com/user-attachments/assets/d8a8ee97-b66e-44be-894f-1913aa89cce0" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="809" height="305" alt="image" src="https://github.com/user-attachments/assets/60c35810-6116-4d90-918d-b0448efb5a34" />

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

<img width="634" height="145" alt="image" src="https://github.com/user-attachments/assets/b20be05b-687b-4ca3-8014-e5d5fe33bb2e" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="162" height="80" alt="image" src="https://github.com/user-attachments/assets/0a6f2b8d-0fb5-4f67-a11c-8af152f26a43" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="162" height="80" alt="image" src="https://github.com/user-attachments/assets/8cfacd8b-a810-4875-a1d3-4165a65c992c" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="162" height="80" alt="image" src="https://github.com/user-attachments/assets/8995c96f-2a86-46c3-9930-ec189f9e9e15" />


tar -xvf backup.tar
## OUTPUT
<img width="162" height="80" alt="image" src="https://github.com/user-attachments/assets/9843dd32-69be-4ecb-be28-a2baf68e6973" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="1265" height="175" alt="image" src="https://github.com/user-attachments/assets/901fdd32-7a6a-4de9-9e0a-74df237414b5" />

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
<img width="409" height="115" alt="image" src="https://github.com/user-attachments/assets/aab88109-c479-4f6a-bdaa-8d5b97e2ccce" />


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
<img width="535" height="412" alt="image" src="https://github.com/user-attachments/assets/07b1be09-cc37-4292-9c28-ddaaeed1c1fd" />

 
ls file1
## OUTPUT
<img width="354" height="59" alt="image" src="https://github.com/user-attachments/assets/f5071cc0-ffb5-478b-ab84-cbe5fb77c605" />

echo $?
## OUTPUT 
<img width="327" height="64" alt="image" src="https://github.com/user-attachments/assets/b959dc71-0a89-4464-bbbd-bb6edecda538" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="351" height="56" alt="image" src="https://github.com/user-attachments/assets/4e5ed01d-7d1f-4661-bcc0-4a98c29cc7dd" />
 
abcd
 
echo $?
 ## OUTPUT
<img width="576" height="270" alt="image" src="https://github.com/user-attachments/assets/39546e52-2716-450a-9ef3-0e2e74939b8d" />


 
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
<img width="595" height="298" alt="image" src="https://github.com/user-attachments/assets/23226c46-2d6a-4bee-83e3-ffe6784d53aa" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="901" height="273" alt="image" src="https://github.com/user-attachments/assets/b3dcbe86-0123-427a-9daf-1794bbd05ea2" />


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
<img width="780" height="314" alt="image" src="https://github.com/user-attachments/assets/0662465b-0215-4895-b5bb-99df266b2539" />

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

<img width="644" height="483" alt="image" src="https://github.com/user-attachments/assets/ad3b51ec-9667-4ea4-b934-de42eb7aad0a" />


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
<img width="648" height="475" alt="image" src="https://github.com/user-attachments/assets/abe1e976-3364-4f2a-a2c4-8ff69d0a29d0" />

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
<img width="712" height="587" alt="image" src="https://github.com/user-attachments/assets/7345cb16-1f47-41df-9d8c-b2db6ffae122" />

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
<img width="709" height="588" alt="image" src="https://github.com/user-attachments/assets/6d2f85eb-b7ad-42a4-a75b-be195883e8ad" />


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
<img width="663" height="308" alt="image" src="https://github.com/user-attachments/assets/e0967c33-ee87-4d57-9c06-f968f8e7cff6" />

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
<img width="627" height="195" alt="image" src="https://github.com/user-attachments/assets/1c79ddf3-3847-4c8a-845d-6141a86dc46d" />

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
<img width="549" height="249" alt="image" src="https://github.com/user-attachments/assets/5bd54e52-2f01-4c93-a421-75017717095c" />


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
<img width="491" height="254" alt="image" src="https://github.com/user-attachments/assets/c773953d-dde9-4ef7-8de5-acd3e912b083" />

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
<img width="469" height="254" alt="image" src="https://github.com/user-attachments/assets/36785b5b-1919-44f0-8b58-1e76531ef192" />

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
<img width="521" height="249" alt="image" src="https://github.com/user-attachments/assets/e29703b1-0afe-4499-93fb-f15d139887ff" />

 
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
 <img width="927" height="344" alt="image" src="https://github.com/user-attachments/assets/2f3b5f9d-e981-4542-a2fd-ab9fa9ce0782" />

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
<img width="595" height="173" alt="image" src="https://github.com/user-attachments/assets/420e0db1-2b3c-486f-b0f3-a807a5bb98ce" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="930" height="168" alt="image" src="https://github.com/user-attachments/assets/49ecad02-b6e2-40bf-ae20-d7839287487d" />



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
<img width="937" height="56" alt="image" src="https://github.com/user-attachments/assets/ba63e7d4-8cc4-4d4b-ad7c-078b70274af5" />

 
 ./funcex.sh 1 2
<img width="948" height="44" alt="image" src="https://github.com/user-attachments/assets/4bfdb841-caa5-44a8-a027-07b2f0b499dd" />

 
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
<img width="944" height="75" alt="image" src="https://github.com/user-attachments/assets/cafa7712-4a83-4830-bf4a-bbdf463295be" />

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
<img width="947" height="105" alt="image" src="https://github.com/user-attachments/assets/ca2de23c-c92d-4780-8c45-0c1093eea030" />

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

 ./argshift.sh 1 2 3
<img width="966" height="271" alt="image" src="https://github.com/user-attachments/assets/62ca4de7-f451-459e-95ae-c6f270e1bc29" />

 
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
<img width="952" height="406" alt="image" src="https://github.com/user-attachments/assets/6adbbab9-a5c7-40b7-9a69-6baefd31ca0c" />
 
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
<img width="961" height="84" alt="image" src="https://github.com/user-attachments/assets/fb9d73c2-07cd-4ac5-a270-99205e420191" />


# RESULT:
The Commands are executed successfully.
