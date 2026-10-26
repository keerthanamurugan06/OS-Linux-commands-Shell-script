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

<img width="386" height="147" alt="image" src="https://github.com/user-attachments/assets/8045260e-c5d8-43dc-bb67-4c3364aecc85" />


cat < file2
## OUTPUT
<img width="386" height="180" alt="image" src="https://github.com/user-attachments/assets/3074b4ed-784d-4d51-a174-17cf6c9ddbf8" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="472" height="302" alt="image" src="https://github.com/user-attachments/assets/352f8a12-91b9-43c9-8257-1ddd5906a2d6" />

comm file1 file2
 ## OUTPUT
<img width="425" height="222" alt="image" src="https://github.com/user-attachments/assets/014c31ed-62fb-44e9-afbd-9111458e55ce" />

 
diff file1 file2
## OUTPUT

<img width="486" height="275" alt="image" src="https://github.com/user-attachments/assets/84105db9-3f58-487c-8fdb-07a8b27d5fdd" />

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


<img width="595" height="182" alt="image" src="https://github.com/user-attachments/assets/337c1173-e1cc-478b-b35d-53d8cb2655c6" />



cut -d "|" -f 1 file22
## OUTPUT


<img width="496" height="186" alt="image" src="https://github.com/user-attachments/assets/f3454c3b-1a20-479b-906a-dedbcceb6b8f" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="613" height="178" alt="image" src="https://github.com/user-attachments/assets/fe2a39af-d138-4e74-aced-fec8eca5c531" />


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

<img width="487" height="107" alt="image" src="https://github.com/user-attachments/assets/7364ae89-e249-4618-9c0e-49f048db458d" />



grep hello newfile 
## OUTPUT



<img width="502" height="102" alt="image" src="https://github.com/user-attachments/assets/5a6b5d8c-b0af-40f7-a1b8-3747c14ec995" />


grep -v hello newfile 
## OUTPUT


<img width="511" height="113" alt="image" src="https://github.com/user-attachments/assets/43497aaa-1295-4551-af00-30eaebf93e0a" />


cat newfile | grep -i "hello"
## OUTPUT




<img width="582" height="146" alt="image" src="https://github.com/user-attachments/assets/eb55b44a-7c69-464f-b91c-d21646d0fdc7" />

cat newfile | grep -i -c "hello"
## OUTPUT



<img width="618" height="107" alt="image" src="https://github.com/user-attachments/assets/fe0ce207-2212-4467-8b47-97e6665de1c6" />


grep -R ubuntu /etc
## OUTPUT
<img width="663" height="392" alt="image" src="https://github.com/user-attachments/assets/675826c1-9526-4bb1-a095-b75cdc471bfd" />

grep -w -n world newfile   
## OUTPUT



<img width="527" height="156" alt="image" src="https://github.com/user-attachments/assets/1be00ef3-fdbc-4228-bdb6-050ced8ad80c" />

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


<img width="567" height="156" alt="image" src="https://github.com/user-attachments/assets/fdfeb731-c527-4f44-b917-abafe31ced93" />


egrep -w '(H|h)ello' newfile 
## OUTPUT


<img width="590" height="145" alt="image" src="https://github.com/user-attachments/assets/05ecf59a-81dd-4b32-9c87-99bc92f89ddc" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="627" height="138" alt="image" src="https://github.com/user-attachments/assets/141ab3d0-e124-4c77-ad90-35c521492869" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="676" height="103" alt="image" src="https://github.com/user-attachments/assets/f4349c19-3cf6-4a74-b432-3a04a46aaa15" />


egrep '(world$)' newfile 
## OUTPUT


<img width="522" height="145" alt="image" src="https://github.com/user-attachments/assets/e1330460-0410-448e-b730-1f0656645768" />

egrep '(World$)' newfile 
## OUTPUT

<img width="527" height="126" alt="image" src="https://github.com/user-attachments/assets/f9854707-448e-495d-aa13-993b34532204" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="557" height="183" alt="image" src="https://github.com/user-attachments/assets/4f4ba51e-e1ab-459a-b186-003385c0f96d" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="557" height="107" alt="image" src="https://github.com/user-attachments/assets/5cea30f8-fea1-4b59-ba90-f00516c4b0a4" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="552" height="105" alt="image" src="https://github.com/user-attachments/assets/043170e4-adc0-4823-850a-110ddd22c56d" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="556" height="107" alt="image" src="https://github.com/user-attachments/assets/90758f8b-e371-498f-a93b-9ee1e31e8bc7" />

egrep l{2} newfile
## OUTPUT

<img width="556" height="132" alt="image" src="https://github.com/user-attachments/assets/dfe72793-0194-4266-9364-b577a6d38f02" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="562" height="172" alt="image" src="https://github.com/user-attachments/assets/e566531f-edea-4a80-bf8b-3884f8759ee3" />

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
<img width="507" height="101" alt="image" src="https://github.com/user-attachments/assets/39377641-5c57-46a5-b2e6-195cc5cf283c" />


sed -n -e '$p' file23

## OUTPUT

<img width="500" height="97" alt="image" src="https://github.com/user-attachments/assets/ab5f99b0-d884-4d9e-9814-5b7bb87c033d" />

sed  -e 's/Ram/Sita/' file23

## OUTPUT

<img width="567" height="372" alt="image" src="https://github.com/user-attachments/assets/7a597d76-ea3a-43a2-9f03-76e98cd3bb88" />


sed  -e '2s/Ram/Sita/' file23

## OUTPUT


<img width="643" height="352" alt="image" src="https://github.com/user-attachments/assets/1ecfbc2f-3773-4824-8aaf-30cbe6abe3b5" />

sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="666" height="370" alt="image" src="https://github.com/user-attachments/assets/7c2c6040-8153-4b1d-b68e-35e5c066752f" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="548" height="245" alt="image" src="https://github.com/user-attachments/assets/4b7dc36e-3834-4a5e-96cc-32dc4a37f40c" />


sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="578" height="192" alt="image" src="https://github.com/user-attachments/assets/f8b5652e-6f34-4c09-8845-37e18f2fc857" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


<img width="638" height="148" alt="image" src="https://github.com/user-attachments/assets/441ea3fd-a67a-49b2-bef8-f553dd38febf" />

seq 10 
## OUTPUT

<img width="551" height="441" alt="image" src="https://github.com/user-attachments/assets/a178274d-a707-4eaa-ae00-042095d5d910" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="501" height="177" alt="image" src="https://github.com/user-attachments/assets/192ac69d-43a7-4df5-931a-96b3badb5d04" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="561" height="180" alt="image" src="https://github.com/user-attachments/assets/40f34494-9ec4-4b80-89c0-e110570d3685" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="532" height="208" alt="image" src="https://github.com/user-attachments/assets/2b473357-e317-4612-812f-436b90ff4dd8" />



seq 2 | sed '2i hello'
## OUTPUT

<img width="517" height="181" alt="image" src="https://github.com/user-attachments/assets/9d884895-69d9-4415-9578-eb067a07ed25" />

seq 10 | sed '2,9c hello'

## OUTPUT

<img width="275" height="76" alt="image" src="https://github.com/user-attachments/assets/5a7a1dfe-5f49-4f7e-a274-d85f151f3b8b" />


sed -n '2,4{s/^/$/;p}' file23

## OUTPUT

<img width="543" height="187" alt="image" src="https://github.com/user-attachments/assets/0ffb413c-992e-4a8d-a4f7-60c97362f304" />


sed -n '2,4{s/$/*/;p}' file23

##OUTPUT

<img width="568" height="187" alt="image" src="https://github.com/user-attachments/assets/156e5bb5-a84b-4495-9fad-1e1c77d57f3c" />

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

<img width="220" height="86" alt="image" src="https://github.com/user-attachments/assets/0f7d2c84-1d6a-4c7a-873e-a6114fee0438" />

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

<img width="615" height="257" alt="image" src="https://github.com/user-attachments/assets/e48ec27e-38c4-4a0f-a0c6-73cf0d2ac126" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="657" height="347" alt="image" src="https://github.com/user-attachments/assets/07e24606-eebd-4c1c-9603-353c9320fb25" />

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

<img width="513" height="190" alt="image" src="https://github.com/user-attachments/assets/3232b48b-72c1-4eae-933e-db18062b3434" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="681" height="182" alt="image" src="https://github.com/user-attachments/assets/e26f7439-a20c-4a29-a97f-08a4e1044c6e" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="555" height="750" alt="image" src="https://github.com/user-attachments/assets/f8953cec-8e0f-4541-8d00-7fa70fea63d8" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="757" height="741" alt="image" src="https://github.com/user-attachments/assets/032c0bb3-a50d-4639-92c5-987dd00a9ca5" />


tar -xvf backup.tar
## OUTPUT
<img width="696" height="718" alt="image" src="https://github.com/user-attachments/assets/498639f6-69da-4601-8db2-2f88c4db382b" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="426" height="117" alt="image" src="https://github.com/user-attachments/assets/af3288be-6d5c-4ded-854b-b27fecc9d0f3" />


gunzip backup.tar.gz
## OUTPUT
<img width="390" height="57" alt="image" src="https://github.com/user-attachments/assets/e0054f7b-f996-4b7f-a595-0c61e68cc076" />


 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="421" height="163" alt="image" src="https://github.com/user-attachments/assets/93e78375-74c7-4d34-b725-f7a046d87b9a" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="558" height="146" alt="image" src="https://github.com/user-attachments/assets/a246587b-8c6e-4f19-a440-12fd6264cc80" />

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
<img width="680" height="368" alt="image" src="https://github.com/user-attachments/assets/ff1ce509-8b07-46b1-874d-c59f987e74b5" />

 
ls file1
## OUTPUT
<img width="425" height="75" alt="image" src="https://github.com/user-attachments/assets/54af5b74-5ca7-4910-ac0f-f6208da80fea" />

echo $?

./one
bash: ./one: Permission denied
## OUTPUT 
 <img width="445" height="76" alt="image" src="https://github.com/user-attachments/assets/5e093d0f-74d4-4fd0-a44d-2392b8d832c4" />

echo $?
## OUTPUT 
 <img width="445" height="76" alt="image" src="https://github.com/user-attachments/assets/3cf8dac6-10e8-4dd6-8302-0cca60a08b39" />

abcd
 
echo $?
 ## OUTPUT

<img width="468" height="67" alt="image" src="https://github.com/user-attachments/assets/e700e1e6-d322-44c1-ac44-f9207fae73dc" />

 
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
<img width="483" height="70" alt="image" src="https://github.com/user-attachments/assets/743b152e-4b95-48c8-9696-210077f80d65" />


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
<img width="430" height="60" alt="image" src="https://github.com/user-attachments/assets/6228aadb-ae26-4eb7-8d74-fa561764c53e" />

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

<img width="471" height="105" alt="image" src="https://github.com/user-attachments/assets/ac754cf6-cf84-4080-adb6-15c9eed8bdfb" />


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

<img width="593" height="125" alt="image" src="https://github.com/user-attachments/assets/ea710b46-55e8-4a94-9f31-7437bdf527ba" />

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

<img width="471" height="105" alt="image" src="https://github.com/user-attachments/assets/ac754cf6-cf84-4080-adb6-15c9eed8bdfb" />

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

<img width="703" height="91" alt="image" src="https://github.com/user-attachments/assets/19cfe216-1d2f-4d4c-a19c-a2454df87d72" />

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

<img width="682" height="100" alt="image" src="https://github.com/user-attachments/assets/ebf1387c-7958-49a3-8b7e-e2363fe966c1" />

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

##OUTPUT

 <img width="480" height="76" alt="image" src="https://github.com/user-attachments/assets/0eb88436-7830-4504-8567-bfeeb90ad3f0" />

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

##OUTPUT

<img width="605" height="290" alt="image" src="https://github.com/user-attachments/assets/b215308f-c164-43a6-bfe1-4b47329a7c03" />

 
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

##OUTPUT

 <img width="400" height="127" alt="image" src="https://github.com/user-attachments/assets/4303f39b-e4a0-4f55-965c-8badcadfa1ee" />

 
 
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

 ##OUTPUT
 <img width="372" height="185" alt="image" src="https://github.com/user-attachments/assets/a9a61ed3-6885-446f-b74b-569125742bb9" />

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

##OUTPUT

<img width="447" height="117" alt="image" src="https://github.com/user-attachments/assets/81e47c28-e960-44a6-a1ad-3552427c79e7" /> 

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

##OUTPUT

<img width="447" height="117" alt="image" src="https://github.com/user-attachments/assets/81e47c28-e960-44a6-a1ad-3552427c79e7" />

 
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

 ##OUTPUT
 
 <img width="678" height="241" alt="image" src="https://github.com/user-attachments/assets/77d86a4e-d70f-4c43-a258-b492c48541ec" />

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

<img width="372" height="185" alt="image" src="https://github.com/user-attachments/assets/a9a61ed3-6885-446f-b74b-569125742bb9" />

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

<img width="627" height="215" alt="image" src="https://github.com/user-attachments/assets/150f9300-6d15-46f3-b5b3-9152f67a5fac" />


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

<img width="377" height="165" alt="image" src="https://github.com/user-attachments/assets/d6b64d8b-11b6-479b-991d-e1a69f5c2294" />

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

<img width="595" height="177" alt="image" src="https://github.com/user-attachments/assets/694df7f5-ae7e-41ae-9305-ecd5acae481c" />

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

 <img width="580" height="335" alt="image" src="https://github.com/user-attachments/assets/a2e970b0-e083-48d5-b572-52f7e9b1d1dc" />

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

 <img width="515" height="90" alt="image" src="https://github.com/user-attachments/assets/78c8b064-93b7-481c-8a1f-a32d1150d574" />

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

<img width="563" height="150" alt="image" src="https://github.com/user-attachments/assets/cfbc52e7-e65d-4e83-86d4-9a2c0be52390" />

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

<img width="427" height="97" alt="image" src="https://github.com/user-attachments/assets/67321934-e23b-425a-a180-3451987eb467" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="450" height="107" alt="image" src="https://github.com/user-attachments/assets/7b114eff-8a1d-4dce-af6c-21f8a7330ed0" />



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
 
##OUTPUT

 <img width="507" height="160" alt="image" src="https://github.com/user-attachments/assets/f3228600-70a5-4cba-a4b6-ffd5d33983a3" />

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

<img width="435" height="122" alt="image" src="https://github.com/user-attachments/assets/cbed0424-a6a7-4528-abce-a33415da83d3" />

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

<img width="506" height="122" alt="image" src="https://github.com/user-attachments/assets/27eab6d7-6c65-45fa-add1-4e18bf179966" />

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
 
 <img width="570" height="392" alt="image" src="https://github.com/user-attachments/assets/6b918c8f-62f3-4259-a292-297f0b5e410b" />

 
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

<img width="495" height="352" alt="image" src="https://github.com/user-attachments/assets/d28dd140-c8d3-49e4-bd2c-6e69f737e3de" />

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

<img width="461" height="111" alt="image" src="https://github.com/user-attachments/assets/230b554c-203d-4e5e-a08a-40021067f1fd" />


# RESULT:
The Commands are executed successfully.
