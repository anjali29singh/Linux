pwd -> present working directory

ls -> list files and directories
cd -> change directory
cd .. ->change directory to one level up

cd / -> change to root directory

cd /directory_name

ls -a or ls --all -> list all including hidden file and directories

ls --help

ls -l -> list directories and files in long format

cd ~ -> change directory to user home directory

which ls -> tells where ls is stored

ls --ignore file_name -> ignore file while listing

ls --ignore=file_name -> ignore files while listing

~ -> this is tilda

echo hello world -> this will output whatever is written after echo

!! and enter, it'll run the last command you ran . !! is called bang

cat file_name -> display contents inside file

while writing some commands and want to jump
CTRL + A takes you to the beginning of the line
CTRL + E – takes you to the end of the line
CTRL + K – "yank" everything after the cursor
CTRL + U – "yank" everything before the cursor
CTRL + Y - "paste" (paste in quotes because it doesn't actually go into your system clipboard) everything you yanked
CTRL + L - clear the screen
CTRL + R – reverse search through history

ps (process snapshot)-> list all processes

pid -> process id . every process or command running has id

sleep n -> wait for n seconds

& -> run processes in background

sleep -n & -> run sleep in background

to pause a running process -> CTRL + Z

jobs -> notice process is stopped

bg (background)-> resume process in the background

fg (foreground)

less -> used to read file

more -> also read content of file

man -> manual

man less -> gives manual of less

tail -> last line of file and outputs it

head -> reads first line of file and outputs it

//creating and moving files

touch file_name -> if file doesn't exist then creates it

rm -> remove files
rm -r -> remove directory or rm -rf (remove force) \

rm -i -> ask permission to delete files in folder

cp source destination -> copy

//output streams

echo "first-text" 1>text.py -> redirect "first-text" into text.py
echo "second-text" 1>text.py -> replace already present content with "second-text"

cat text.py 1> new-text.py -> replace contents of new-text.py to text.py
cat text.py 1>> new-text.py -> instead of replace , this appends
//appending >>

//stderr : to redirect error 2>>

cat hello-text.py 2 > text.py -> hello-text is not found therefore error is redirected to text.py

//input streams
grep -> allows you to find text in file

grep "hello" <hello.txt

ps aux -> outputs all processing running

//connecting two machines via ssh key

//1. generate public private key pair
ssh-keygen -t rsa

//2.enter file in which to save the key

//3. enter passphrase : this is used for encriptying private key

//if passphrase is empty then it will save private key as id_rsa and public key as id_rsa.pub

cat ~/.ssh/id_rsa.pub

//create .ssh directory in second machine

// copy id_rsa.pub in a file inside .ssh folder from 1st machine to second machine

//adding permissions in second machine

chmod 700 ~/.ssh

chmod 600 ~/.ssh/authorized_keys

// ifconfig gives out bunch of addresses and hashes.

// ip adress of inet

ssh anjali@<the ip address you just got from ifconfig on the other machine>

//sftp to transfer files between local and vm
sftp anjali@<ip>

lpwd : local present working directory
lcd : change local directory
lls : list local pwd
! : can be used to run commands locally

put hello.txt helloworld.txt : transfer hello.txt file from local to host

get hello.txt helloworld.txt : download file to local from host

//Create Vms in ubuntu using multipass

multipass launch <instance name>

multipass shell <instance name>

multipass stop <instance name>

multipass delete <instance name>

multipass purge # to completly remove
