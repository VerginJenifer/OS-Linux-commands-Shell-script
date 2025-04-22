
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

![image](https://github.com/user-attachments/assets/d3622404-d369-4bb2-84c5-670b568e94d3)


cat < file2
## OUTPUT
![image](https://github.com/user-attachments/assets/147ce091-5cb0-4559-a785-7021b0b29fd6)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![image](https://github.com/user-attachments/assets/d0a1bf06-5c04-44b6-97e4-1255382c0db7)

comm file1 file2
 ## OUTPUT
![image](https://github.com/user-attachments/assets/5b81657e-8b28-4ddb-b59e-d7b53e0fda5e)

 
diff file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/85fad8c2-5e22-4695-92e5-44ef1dca5aa2)


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

![image](https://github.com/user-attachments/assets/0fccf73e-088b-4780-ad6e-94432f67e302)



cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/0a4f40b4-902e-433a-a1ad-5e646dbb1f75)



cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/12a73dca-8aff-482f-8014-4a724e2bec8c)


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
![image](https://github.com/user-attachments/assets/1b135735-0edf-458c-9bc3-3752c390655c)



grep -v hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/02eb02be-1c80-4a3a-9059-0c9a09be80e4)



cat newfile | grep -i "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/ff46a800-b406-478e-9986-6ee356ccd71f)



cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/eeecb567-feac-45c7-b615-91297a196d57)




grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/user-attachments/assets/4f31b6e5-184b-4cb1-bd3a-227d1ba63320)



grep -w -n world newfile   
## OUTPUT
![image](https://github.com/user-attachments/assets/390de593-8be0-412f-9c42-08ba948d4a73)


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
![image](https://github.com/user-attachments/assets/7ad9e11c-d957-4b23-9899-db6dbffb042d)



egrep -w '(H|h)ello' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/d57c2c9e-cad8-4e83-bd7b-48499b7c530f)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/f598dee8-fa9a-4a9b-8fcc-193834548f6d)



egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/6a2a6790-e522-4585-b3bb-95a6abf072a7)



egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/f3659550-edfd-4f4a-a0ad-cfe0c6290ecb)



egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/a3976e41-2201-42d2-88c7-2f9f6e550f1d)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/637abaa2-8afe-4c81-88bc-a9046b25d422)



egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/b717076b-2705-46a7-b731-4ccaf897aac1)



egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/4d7daa07-683d-48cb-857c-c725c7e2ed57)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/e0adefd4-a752-4c3f-878a-a66ac82d9810)


egrep l{2} newfile
## OUTPUT
![image](https://github.com/user-attachments/assets/cce3141b-e01c-4521-b07f-be6e07fc0264)



egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/user-attachments/assets/85fb20f6-48d7-41c4-92b9-a7ac8a3ae2fc)


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
![image](https://github.com/user-attachments/assets/31f3cf5e-f22a-4333-9dcc-7f5e9347737b)



sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/04a6112d-ecfb-4648-8d31-503da5c07d2e)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/f414b534-10ce-40f8-9fc6-1f05cfe9aaf1)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/b9921409-35ad-4097-a5c8-53714e5af765)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/8519591d-859f-4b5a-9763-b70e818ffaa3)



sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/6fa20ff1-0308-431e-a639-0598765fb2a3)



sed -n -e '2,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/56ad3f30-61c3-4572-8098-419f990950ed)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/96d822cf-6803-452d-a841-3904f5537279)



seq 10 
## OUTPUT
![image](https://github.com/user-attachments/assets/8e655157-4c98-447a-b199-040b46cd3da4)



seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/user-attachments/assets/cf86c8a5-0776-4450-9a85-715b240ac8dd)



seq 10 | sed -n '2,~4p'
## OUTPUT

![image](https://github.com/user-attachments/assets/3cb70fab-7934-41dd-be37-5f632490cc1e)


seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/d269e9cc-5879-455d-a89a-8bc62719695c)



seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/e226978d-d34b-4550-89df-3a500a2d3f3c)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/17c786dc-62bf-4226-87c0-0107dfbb0bfa)



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/0b6cfd32-023b-4742-93ce-8acd7cd3513d)



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/f2c3ac14-4f8b-4145-99bd-331b746c24a5)


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
![image](https://github.com/user-attachments/assets/b4cc690e-3573-40f0-a339-ee7b9fd71b34)


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
![image](https://github.com/user-attachments/assets/464afd91-cb48-4509-a69d-8630811f03a4)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 ![image](https://github.com/user-attachments/assets/b7908896-6afa-4e19-ade1-21bd5ab0d09e)


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
![image](https://github.com/user-attachments/assets/78a370e0-f76d-41e5-b70c-d9506f6f62f9)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/user-attachments/assets/81ff1746-4303-48ac-a668-a4424d1ad738)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/user-attachments/assets/4259d4b0-ba15-48f2-9e7b-1fc0c4fb837c)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/dd48c893-8343-4bda-af4d-387346dc0a3c)


tar -xvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/f728db45-e68a-48f1-8161-411e0339574b)

gzip backup.tar

ls .gz
## OUTPUT
 ![image](https://github.com/user-attachments/assets/29970a68-b3e5-4892-b107-027cd0c1de0d)


 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![image](https://github.com/user-attachments/assets/ac832853-a09e-4585-bfa8-d70030fbcd30)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/user-attachments/assets/54675266-5ea4-4992-a77c-c5750cd35070)


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
![image](https://github.com/user-attachments/assets/3ec16e52-e67f-469f-84a0-84fe3845c155)

 
ls file1
## OUTPUT
![image](https://github.com/user-attachments/assets/d24968ba-61ee-415a-a4ae-7c7790beb815)

echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/6973e88b-14a9-4a97-91a3-eb368447f7c4)

 
abcd
 
echo $?
 ## OUTPUT
![image](https://github.com/user-attachments/assets/c92beea4-16c5-48b1-a562-c4d0f169c9dc)


 
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
~~~
bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
~~~
##OUTPUT



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/119e08a9-7a86-49a7-8aec-4d1a6604b3a5)


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
![image](https://github.com/user-attachments/assets/bdb1b2f4-184e-457f-85c1-a59f295f002f)

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
![image](https://github.com/user-attachments/assets/7bc60fd4-7fcd-435f-8bd3-7dcc474383f5)



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
![image](https://github.com/user-attachments/assets/ebb4435e-2d7e-463b-9807-52d43620f18f)


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
![image](https://github.com/user-attachments/assets/b95731bf-a6a2-45c6-805e-13eda5480e2e)

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
![image](https://github.com/user-attachments/assets/c26b4108-1755-47a7-b666-6851fcdd0c59)


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
![image](https://github.com/user-attachments/assets/297c89eb-ceb0-4ba8-ad40-df565cd4a07d)

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
![image](https://github.com/user-attachments/assets/e3cde648-548f-48b3-a5db-9d264f1f4c3b)
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
![image](https://github.com/user-attachments/assets/1299e194-551a-4d6f-ad15-f023a64ebb7a)


 
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
![image](https://github.com/user-attachments/assets/a42cdea5-2291-468b-a09b-ac1dec1b8998)

 
 
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
![image](https://github.com/user-attachments/assets/2f39690a-8870-4315-a51e-7e344580cc9c)

 
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
![image](https://github.com/user-attachments/assets/1009b97d-19cd-4828-b404-1d772e16b31e)

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
![image](https://github.com/user-attachments/assets/88b9a32a-58da-4ccb-a54f-6d7537171634)

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
![image](https://github.com/user-attachments/assets/5217f9f6-427f-4ccb-85d1-3bfbf727427e)

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
![image](https://github.com/user-attachments/assets/d45ce04e-991e-4f95-94f0-c37b41c33103)

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
![image](https://github.com/user-attachments/assets/0aef7c6c-9110-49c8-8be8-d2003feaff6f)

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
![image](https://github.com/user-attachments/assets/be5898d3-9ea7-44b5-b47b-9d3267ee6b1d)

 
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
![image](https://github.com/user-attachments/assets/23832aca-eae7-4cc6-8942-771e25ecf2a3)
cat forcontinue.sh

#!/bin/bash
# breaking out of a for loop
~~~
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
~~~
$ chmod 755 forcontinue.sh

$ ./forcontinue.sh

## OUTPUT
 ![image](https://github.com/user-attachments/assets/f0c4b7aa-2ac0-4729-a359-18ec82b12187)

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
![image](https://github.com/user-attachments/assets/05cf13da-1fa0-4959-b0b4-796554685ba6)


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
![image](https://github.com/user-attachments/assets/fac05a67-d40d-4e8a-a95e-58fd38d1fe72)
 
 
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
![image](https://github.com/user-attachments/assets/a9f4e4bc-1b63-4bb1-b315-fe9941763543)

 
 ./funcex.sh 1 2
![image](https://github.com/user-attachments/assets/b18ad93f-43fa-43a8-a971-50f31c1bc49f)

 
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
![image](https://github.com/user-attachments/assets/fa39f88a-dd3b-4831-b795-b6f50bc47603)

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
 ![image](https://github.com/user-attachments/assets/336babf1-e4b3-42cf-a52d-f4749daf3fd1)

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
 ![image](https://github.com/user-attachments/assets/4ab3e047-9bf5-4677-b1b1-54f8a9c11831)

 
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
 ![image](https://github.com/user-attachments/assets/ff5986c3-0c5f-42ff-9e8f-513737e59e90)

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
![image](https://github.com/user-attachments/assets/5b011e01-b4b5-406d-a5b2-6958b5243454)


# RESULT:
The Commands are executed successfully.
