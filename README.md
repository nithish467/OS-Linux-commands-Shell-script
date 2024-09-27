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
![image](https://github.com/user-attachments/assets/216f0e4a-a333-4691-9abb-6821e6e0ffd7)


cat < file2
## OUTPUT

![image](https://github.com/user-attachments/assets/719fb199-f1fa-446e-bb48-6cb7a01c74a8)


# Comparing Files
cmp file1 file2
## OUTPUT

![image](https://github.com/user-attachments/assets/2a99b01d-be4f-4cac-b383-7dd75a646698)

 
diff file1 file2
## OUTPUT

![image](https://github.com/user-attachments/assets/e4daa3fe-5bdc-493d-97d7-f3c793ebca48)


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

![image](https://github.com/user-attachments/assets/202928a1-d7ac-4cf9-b272-31d773f22020)



cut -d "|" -f 1 file22
## OUTPUT

![image](https://github.com/user-attachments/assets/6e4ac64f-78db-4d03-82cd-593fa30f8493)


cut -d "|" -f 2 file22
## OUTPUT

![image](https://github.com/user-attachments/assets/d48b9bc0-a457-4692-b087-273be6b23daf)


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

![image](https://github.com/user-attachments/assets/f4705a24-6f4e-4d3a-819f-5a29d52ec026)


grep hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/bcb4dbc0-0077-43e8-b0f8-1e48a6d93bbb)


grep -v hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/ec05dacd-79db-47d2-a73b-c81d095b5b68)


cat newfile | grep -i "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/a5574bba-39eb-4358-94c0-deb243c745f1)


cat newfile | grep -i -c "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/a3286176-f34b-4d0f-a55b-bb9f0d7aaa58)


grep -R ubuntu /etc
## OUTPUT

![image](https://github.com/user-attachments/assets/f6cf5c1b-ea6e-4d3c-b5d9-f685fd113fe9)


grep -w -n world newfile   
## OUTPUT

![image](https://github.com/user-attachments/assets/e778245d-f571-4b59-afc1-fda0eb8f7239)


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

![image](https://github.com/user-attachments/assets/962e567e-f4ae-421c-a702-128c9bbb7296)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/9c24fbfc-6491-4bef-822a-17bf75cc6692)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/71088dd9-8715-4666-a6b4-9e89b5152ff9)


egrep '(^hello)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/de68eeed-3b6e-40ee-b33d-da3fe283dddc)


egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/6112392c-59d3-466d-845d-41e1c55b7b6c)


egrep '(World$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/c5f2c305-dc30-4b1b-bc02-a3f2198e7f0f)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/58e70839-bcf1-4489-8c2d-0af4eee0e6f5)


egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/b5077470-2a74-4d0b-b19c-bee428641d1b)


egrep 'Linux.*world' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/8047d1bb-b795-4452-8f87-46e599d3405a)


egrep 'Linux.*World' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/0600757a-dd15-47cf-a4b6-4541669d009d)

egrep l{2} newfile
## OUTPUT

![image](https://github.com/user-attachments/assets/237c6346-fba8-4e57-b9da-e108c47dd193)


egrep 's{1,2}' newfile
## OUTPUT 

![image](https://github.com/user-attachments/assets/8188c60c-8fe7-4744-a42a-c255cb2d950e)


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

![image](https://github.com/user-attachments/assets/dc400bca-6dc0-4f78-886b-22774d5db470)


sed -n -e '$p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/98defb45-b900-477e-9fbf-b2de573e7b5f)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/df64b462-d739-4873-b0f5-71953e832505)

sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/8fd9af04-eadc-4d50-9654-7df99d7a2f1a)

sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/049fab77-4244-43f5-bffb-600aa56c9816)

sed -n -e '1,5p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/3a94e556-3b98-418d-b58a-a296de88fca5)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/da2b06a7-b796-4741-8f09-5c85cd9d7664)


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/7985186a-3abf-44f6-ac44-1e05b1fc058d)


seq 10 
## OUTPUT

![image](https://github.com/user-attachments/assets/82a0a339-630f-43fb-bb79-f8ef150fb6b9)
'4,6p'

seq 10 | sed -n 
## OUTPUT

![image](https://github.com/user-attachments/assets/117ec9df-e5e3-4523-9529-45d1f344a1c1)


seq 10 | sed -n '2,~4p'
## OUTPUT

![image](https://github.com/user-attachments/assets/2fccaebf-0dbc-489c-a02e-f4e7f7e0e531)

seq 3 | sed '2a hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/b94765ca-9673-4443-8056-92cd0066bd1d)


seq 2 | sed '2i hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/121d1e8b-70d8-44aa-88fd-dc4cee4e57b8)


seq 10 | sed '2,9c hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/0a560344-4e26-4510-b305-06fbf0c4ba2e)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/8866b145-b48f-4746-aacd-30945f90b0f7)


sed -n '2,4{s/$/*/;p}' file23

## OUTPUT

![image](https://github.com/user-attachments/assets/f1686a07-4d41-4870-a993-f0cb55cda7d1)


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

![image](https://github.com/user-attachments/assets/613722e1-6100-4194-be7d-40f913854a4a)


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

![image](https://github.com/user-attachments/assets/24abdee2-25f2-4f8b-a01a-fa86810baf10)


#Using tr command
cat file23 | tr [:lower:] [:upper:]

 ## OUTPUT

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

![image](https://github.com/user-attachments/assets/627dd41b-e28c-4c54-9b80-c9e4bcf9877b)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![image](https://github.com/user-attachments/assets/898babec-bda6-44d6-9a8a-8478403be580)


#Backup commands
tar -cvf backup.tar *
## OUTPUT

![image](https://github.com/user-attachments/assets/155448f8-d837-4b8c-8846-46575a9148f0)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT

![image](https://github.com/user-attachments/assets/cdf3016b-3f5b-48db-bd85-51515586b761)


tar -xvf backup.tar
## OUTPUT

![image](https://github.com/user-attachments/assets/9a2d5fe4-1073-4353-aa3d-acb59f67805c)


gzip backup.tar

ls .gz
## OUTPUT
 


gunzip backup.tar.gz
## OUTPUT

![image](https://github.com/user-attachments/assets/78060914-7ab0-4163-8aab-d570855dbe6d)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

![image](https://github.com/user-attachments/assets/784dc617-0763-4df2-b02f-87eac5c4ab2c)


cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![image](https://github.com/user-attachments/assets/1b3e3f77-6bba-4018-bf11-bdc3a888646a)


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

![image](https://github.com/user-attachments/assets/84bfb6e2-8952-4148-8c5a-0be52cbf0de1)

 
ls file1
## OUTPUT

![image](https://github.com/user-attachments/assets/fba96ee5-11ed-47c6-9e91-004c08995b87)


echo $?
## OUTPUT 
./one
bash: ./one: Permission denied

![image](https://github.com/user-attachments/assets/e0011c4f-6ee1-4e31-9360-a111e8423213)

 
echo $?
## OUTPUT 
 
![image](https://github.com/user-attachments/assets/fa886ed5-1e74-4309-94b3-a5848f970a2d)


abcd
 
echo $?
 ## OUTPUT

![image](https://github.com/user-attachments/assets/3aa84d2a-04e9-4b97-a721-010084b307c7)

 
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

![image](https://github.com/user-attachments/assets/bea1f9de-c7ac-4b25-ad7f-178119f0d24a)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![image](https://github.com/user-attachments/assets/1c0c1bbf-dc2d-49a2-8811-34ba832bd268)


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

![image](https://github.com/user-attachments/assets/9119b418-5a77-4046-91b0-1d69b5f653c3)

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

![image](https://github.com/user-attachments/assets/9c54482c-6385-404d-be7f-3ea6b070a9d6)


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

![image](https://github.com/user-attachments/assets/ed2955ec-97a0-4390-a49b-85a4ad747a7c)


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

![image](https://github.com/user-attachments/assets/e501572b-74e0-4e2a-8d0c-17f5c705eb73)


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

![image](https://github.com/user-attachments/assets/67bb339f-da42-4cc6-aa2b-52a8219bde5c)

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

![image](https://github.com/user-attachments/assets/fd798f00-50a4-403b-9a7c-b6982d3b3145)


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

![image](https://github.com/user-attachments/assets/27f05f1b-af12-4f40-80cd-bee2ff7dd17c)


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

![image](https://github.com/user-attachments/assets/c642ab00-5ccb-4eed-a7e3-98ec26f87e6b)

 
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
 
![image](https://github.com/user-attachments/assets/d3c27736-c518-420c-8ddf-5202d313d239)


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
 ## OUTPUT

![image](https://github.com/user-attachments/assets/cdecfb8f-61e3-457a-9897-ebb1cae270b2)

 
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
## OUTPUT

![image](https://github.com/user-attachments/assets/ef1c37ba-f696-4793-84f1-2ef0aad7bb39)


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
![image](https://github.com/user-attachments/assets/a7103b18-62f1-4942-ac9a-ed14e8b97a0d)

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

![image](https://github.com/user-attachments/assets/416100d4-4965-4fc3-8c4e-9a00eaf85271)


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

![image](https://github.com/user-attachments/assets/93a1ef5f-2376-440d-96ba-7c455f850bc4)


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

![image](https://github.com/user-attachments/assets/2bbb756b-07db-4729-a49b-a84ce311b3b6)

 
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
$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
 ## OUTPUT

![image](https://github.com/user-attachments/assets/cebd012e-beac-4b23-9600-4950387fd74c)


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
 
![image](https://github.com/user-attachments/assets/9114f51a-e268-4fda-ab1d-534ba06c4f79)


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

![img 1](https://github.com/user-attachments/assets/fd59efcb-654d-40ea-b8a5-eb13e95a9183)



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

![img 1](https://github.com/user-attachments/assets/224a3fb7-5246-4c20-be9e-ae7212e0b701)



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
 
![image](https://github.com/user-attachments/assets/f13c4588-b7d9-43b0-b1d7-dcc4c5381257)

 
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
 ![image](https://github.com/user-attachments/assets/e09bda5f-e170-4b98-848a-ef1dc410ba50)


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

![image](https://github.com/user-attachments/assets/a7ee7378-a133-4ece-8f8c-200124eff847)

 
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
 
![image](https://github.com/user-attachments/assets/0e3ccf28-7b9c-4bc7-8b83-5913e32bd750)



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

![image](https://github.com/user-attachments/assets/ed9ff6bd-43e8-4993-bb32-61793ebed4ee)



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

![image](https://github.com/user-attachments/assets/40fc0f03-cf89-4286-a6eb-d39eb7499ef6)


# RESULT:
The Commands are executed successfully.
