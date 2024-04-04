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

![316389314-e1865b3c-9ba5-4ae3-8130-75314196e683](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/b819a786-7884-4888-8a4d-ee0dcc88b2ed)


cat < file2
## OUTPUT
![316389348-93397153-426e-49ce-b433-c42790615c81](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/bd8e5637-a6e2-44e9-8783-f434da31ccbb)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![316389372-e062edf1-4a63-427b-9a62-37ef061f8eff](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/633569d9-71c7-4390-b50f-79f34325234e)

comm file1 file2
 ## OUTPUT
![316389375-05c49397-217d-4e0e-9e31-981f43ba8ad3](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/ab1d77f2-434f-40b1-87e8-37ec13d19a33)

 
diff file1 file2
## OUTPUT

![316389974-071153b0-4607-477b-9e5f-1b010506a750](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/8501f696-0cef-41c4-a3cf-b2db43ef6d67)

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
![316389750-de3f331a-2bb9-4df2-b857-86cde0cdcd16](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/d34575ea-0e43-4c42-9aa3-8532007c4282)




cut -d "|" -f 1 file22
## OUTPUT

![316389744-e96044a5-af8e-4155-a777-a0b088bae5e5](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/a1b797f2-15d3-4dc4-be17-cb4d2471caa3)


cut -d "|" -f 2 file22
## OUTPUT
![316389732-9215084c-72d8-4339-8278-e6d65b2937ea](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/40ecf597-b109-4396-8ad5-14d73213bec9)


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

![316389687-55f2321a-c935-4db9-a6c0-3ba4ded197e3](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/fafa3204-69e8-4f0c-9836-5e98a13d2060)


grep hello newfile 
## OUTPUT

![316389658-e141ebcc-5eae-4bd7-95eb-4506a9df818a](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/9f9a2b63-7d05-4b37-9d38-786e00e31145)



grep -v hello newfile 
## OUTPUT

![316389591-1ea81849-58ba-4460-bbb8-1eaac3752cf3](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/07336c3f-a3a4-4b31-8529-9bdf2b288363)


cat newfile | grep -i "hello"
## OUTPUT

![316389562-933b3400-135a-4f53-92e8-0301035689af](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/e5b666c3-4d91-4435-ad2f-6b80675af1eb)



cat newfile | grep -i -c "hello"
## OUTPUT

![316389549-a5c1bfa3-ff30-41a0-bc30-0329535288fe](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/25282dfa-afb7-4bd9-943d-0a86917337f1)



grep -R ubuntu /etc
## OUTPUT
![316389520-907a0c95-4309-48ca-ae05-c59845ca3e27](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/34460e72-b86e-41f5-a903-6d7ce804cf0b)



grep -w -n world newfile   
## OUTPUT
![316394861-c9516882-d7fb-4cb2-929f-7c29661c60a5](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/4619daf5-c113-42f6-a410-9ae442a4ff9f)


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

![316393611-d886a2ed-37a9-481e-9bf7-cc2f266e4354](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/b94593cd-eba1-484e-b928-b57467a5cea9)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![316393423-15375789-eaae-40e4-aa81-a16255065ca2](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/f8e2679f-9dee-4c84-acc2-d5eb2525918a)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![316393411-8d2038be-a5bd-4882-902d-98d29fb2dd8d](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/5cc535f8-c74b-4453-8541-66055ff07cdf)



egrep '(^hello)' newfile 
## OUTPUT
![316393278-eb22284b-c1bd-46fb-99a7-c5e6bc0cd7da](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/15b7d907-c828-4897-a8f9-d9bcf7581fb1)



egrep '(world$)' newfile 
## OUTPUT
![316393244-25c8136c-09a6-45ff-952f-e4dd1741ad8e](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/6342b8eb-c55c-4a37-9bb1-cfe801909381)



egrep '(World$)' newfile 
## OUTPUT


egrep '((W|w)orld$)' newfile 
## OUTPUT
![316393204-26d5b2dc-b1e5-4e3f-b27a-ff7bbe596897](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/ac4584e9-e05f-4af8-a680-ecf68aafa8b6)



egrep '[1-9]' newfile 
## OUTPUT
![316393151-d8422c26-cf2a-4254-bd2f-18316763c64b](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/d281c0be-5d71-44d4-8ceb-c4be322ecc2c)



egrep 'Linux.*world' newfile 
## OUTPUT

![316393041-cfcdb071-faa8-4301-9463-782814ff7b94](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/a68c7fe1-926d-4a3c-ac56-40e2b564876d)

egrep 'Linux.*World' newfile 
## OUTPUT
![316393015-3f7edf2b-93b2-48e6-9f24-362b4dec42f9](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/f13756bb-6bb9-4ff7-b947-062658197e56)


egrep l{2} newfile
## OUTPUT

![316392991-e0a6d95f-f3dc-4404-a6a4-a304c475df22](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/a4d0be7a-2a5e-4b4e-8de4-1bc0bbb11b88)


egrep 's{1,2}' newfile
## OUTPUT 
![316392966-b66f6083-34b1-48ee-bb6c-aab952faec08](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/a5f7d28d-c4ef-4216-a72b-a0c3933f2d95)


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

![316392906-4087e342-6d0d-4a29-91c6-32b449cc6768](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/c9c82a10-c9db-4a20-9376-33d922ef0efc)


sed -n -e '$p' file23
## OUTPUT
![316392838-7c1c1260-8d28-441c-b2bd-73c4e17a5fc6](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/2a939fb3-a40e-4e71-9408-6286642d391b)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![316392812-dfde99f0-fa3c-4ee9-9308-4b156fbb6f19](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/909ca139-de0e-4de8-a816-5019e8a5e5d0)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![316392607-94f9b8e5-12cb-44c6-bd55-20afef336f33](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/3a04ee50-dda2-47f2-92e8-d7cb0290162c)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![316392533-e343e5fa-f4d3-4e67-bef2-a5f03724e8cc](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/e3708d2e-d6d3-4807-b391-e4a5610e02ed)


sed -n -e '1,5p' file23
## OUTPUT
![316392357-03e49e12-01a0-4e2d-9222-9b828fa5e625](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/83ff50f2-f53c-412e-9675-6ff05d34f7e9)



sed -n -e '2,/Joe/p' file23
## OUTPUT

![316392273-cc066302-85e9-411c-8e4c-78d2d947b99b](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/d699eef1-4448-48d8-83ea-e39f047f5e18)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![316392225-c8f94558-cc4c-48c2-acdc-33ce86aafaf1](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/54e9e3b6-230a-46e8-a355-5276d9469d0c)


seq 10 
## OUTPUT
![316392094-1ee2a815-d4fc-4ff2-a59b-c14a74634867](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/b58c3eb7-e7f5-4107-8002-9e6b59a49263)



seq 10 | sed -n '4,6p'
## OUTPUT
![316391983-e56ed090-4f4f-4d82-a643-2025d2ab0bea](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/d714c6a9-0713-45be-b6f0-918311c3aabb)



seq 10 | sed -n '2,~4p'
## OUTPUT
![316391911-46709a93-225d-44e6-8349-fe29796d2d5c](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/a45c7192-b622-4b56-acc9-5bc36a422483)



seq 3 | sed '2a hello'
## OUTPUT

![316391812-e11a6367-6206-4d6c-9994-0aeb589941eb](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/e0047958-0c5d-497b-8631-2600da01af75)


seq 2 | sed '2i hello'
## OUTPUT

![316391792-be2a6191-c0af-49f5-b1b2-b914b2346679](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/c5998850-c33b-4ed9-bbbe-2f930ad7b1be)

seq 10 | sed '2,9c hello'
## OUTPUT

![316391738-8aba6349-ac13-468a-9ff4-fccdf4cfe7bb](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/fb2c4ca1-42ad-438b-80db-f6f225be2819)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![316391700-1366e637-0936-4835-ade7-828cdc0cf9c6](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/cbb4758e-c511-4bea-a1fe-b4a6604abd85)


sed -n '2,4{s/$/*/;p}' file23
![316391510-81d415b2-296d-4f18-8bfd-63a0a612508a](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/a68cc99f-acae-453b-b6b1-3258d5cb4162)


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
![316391376-442de1b3-bb1e-4d39-9c94-97063f9eac81](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/5cf920c8-b1ac-40c2-880b-2fd2a3b8e32a)


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
![316391273-3d563768-5240-43a1-b0c4-69b65ea5c6f1](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/d40de376-d3ba-429a-bc49-c73da90da7f1)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![316391126-327b277e-56c9-4a8e-aea7-f6225f1f6060](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/1fb1ea6a-a695-4784-af45-554b7d454c77)

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

![316391037-5f4bd05b-cbbf-4233-83e4-65aef6bdd135](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/b9147c65-f65c-4d9e-9d6b-011b09a06f75)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![316390975-8a7259ee-0f46-4862-b9cd-4721c9d8d8c6](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/71833c7f-7785-4720-9ee1-ee522ee27bd1)

#Backup commands
tar -cvf backup.tar *
## OUTPUT
![316390888-f1995523-039c-4bab-93ca-3c4fc400bc80](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/9e040e65-aed7-4804-90ce-f333ce00eb3f)

cat << stop > herecheck.txt

hello in this world

i cant stop

for this non stop movement

stop

cat herecheck.txt
## OUTPUT

![316390779-d39be17a-18da-4c6d-9ba1-3cbe6809b696](https://github.com/logeshwari2004/OS-Linux-commands-Shell-script/assets/94211349/660390eb-29a6-4683-98df-0a7f7366d5a1)



# RESULT:
The Commands are executed successfully.
