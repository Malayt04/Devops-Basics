# Exploring Linux: Understanding Its Architecture and Significance

## Introduction
In the realm of computing, the operating system serves as a vital mediator between the hardware components of a system and the software applications that run on it. This intermediary role is crucial for ensuring seamless communication and efficient utilization of resources. Among the plethora of operating systems available, Linux stands out as a powerful and versatile option, revered for its open-source nature, robust security features, diverse distributions, and exceptional performance. In this comprehensive guide, we delve into the fundamental aspects of Linux, elucidating its architecture and highlighting the reasons behind its widespread adoption.

## The Role of an Operating System
Before delving into the specifics of Linux, it's essential to grasp the fundamental role of an operating system in the computing ecosystem. Essentially, an operating system serves as a bridge between the hardware components of a device (such as a laptop or server) and the software applications that users interact with. Without an operating system, software programs would be unable to directly communicate with the underlying hardware, leading to inefficiencies and a lack of coordination.

## Why Choose Linux?
Linux has garnered immense popularity and acclaim for several compelling reasons:

### 1. Free and Open Source:
Linux is distributed under open-source licenses, meaning that users have access to its source code and can modify, distribute, and enhance it as per their requirements. This not only fosters a collaborative development environment but also eliminates the need for expensive licensing fees, making Linux an economical choice for individuals and organizations alike.

### 2. Robust Security:
Security is paramount in today's digital landscape, and Linux is renowned for its robust security features. Its inherent design principles, such as granular user permissions, robust privilege separation, and timely security updates, contribute to its resilience against malware, viruses, and other cyber threats.

### 3. Diverse Distributions:
One of the most appealing aspects of Linux is its diverse array of distributions, or "distros," each tailored to specific use cases, preferences, and requirements. Whether you're a beginner seeking a user-friendly experience or a seasoned developer craving customization and control, there's a Linux distribution suited to your needs.

### 4. Exceptional Performance:
Linux is engineered for speed and efficiency, leveraging its lightweight design and optimized kernel to deliver exceptional performance even on modest hardware configurations. This makes it an ideal choice for resource-constrained environments and high-performance computing tasks alike.

# Basic Architecture of Linux
At its core, Linux comprises several essential components that collectively form its architecture:

## 1. Kernel:
The kernel serves as the nucleus of the operating system, responsible for managing hardware resources, facilitating communication between software and hardware, and executing essential system tasks. It provides critical functionalities such as device management, memory management, process management, and handling system-related calls.

## 2. System Libraries:
System libraries are collections of reusable functions and code modules that provide essential functionalities to user applications. These libraries abstract complex operations, such as file I/O, networking, and memory management, simplifying the development process for software developers.

## 3. Compilers:
Compilers are software tools that translate human-readable source code into machine-readable instructions that can be executed by the computer's hardware. In the Linux ecosystem, compilers play a pivotal role in software development, enabling programmers to write, compile, and debug code efficiently.

## 4. User Processes and System Software:
User processes encompass the myriad applications and programs that users interact with on a daily basis, ranging from web browsers and text editors to multimedia players and productivity suites. System software, on the other hand, comprises essential utilities and services that operate behind the scenes, ensuring the smooth functioning of the system.

In essence, the architecture of Linux embodies a symbiotic relationship between its core components, facilitating a seamless interaction between hardware and software while prioritizing performance, security, and flexibility.

# Conclusion
Linux continues to exert a profound influence on the computing landscape, empowering users with a powerful, customizable, and secure operating system that caters to a diverse range of needs and preferences. By understanding its architecture and appreciating its myriad benefits, individuals and organizations can harness the full potential of Linux to drive innovation, productivity, and success in the digital age. Whether you're a seasoned sysadmin, a budding developer, or an avid enthusiast, Linux offers a compelling platform for exploration, experimentation, and mastery.<br>

Now let's look at some of the linux commands 

# Linux Commands for beginners

- `whereis` - Find the path of that executable file.

### List operation
- `ls` - Shows list.
    - `-a` - Hidden file.
    - `-l` - Permission.
    - `-R` - Show sub dir.

### Changing dir operation
- `cd <folder-name>` - Change Dir.
- `cd ..` -   Go one Directory back.
- `cd` -    Go to home.
- `cd ../<foldername>` - Open a previous dir folder.
- `cd <path>` - Open a dir with the path.

### File/Folder Ope.
- `mkdir <new-dir-name>` - Create a new folder.
- `mkdir -p test/test1/test2` - Create a dir between two directories.
- `touch <new-file-name>` - create a blank file.
- `pwd` - Present working directory.
- `cat <filename>` - Display file content.
- `cat > <new-file-name>` - Create a file.
- `dd if=/dev/zero of=bos_dosya bs=4G count=1`- create empty file with zeros
- `cat >> <filename>` - Append the file
- `cat  <filename1> >> <filename2>` - Append the content of the file filename1 at the end of the file <filename2>.
- `cat <filename> <filename2> ` - Display 2 files at a time.
- `cat <filename> <filename2> > <newfile-name>` - Merge both of file content in a single one.
- `cat <file-name> | tr > <new-file-name>` - Translate the file.
- `cut -c  1-2 <filename>` - cut the file column wise
- `echo "Hello" >> <file-name>`
- `man <commad name>` - Know about the command usages and options.
- `man <commad name>` - know about the command.

### File/Folder operation
- `cp <file-name> <new-fie-name>` - Make a copy of a file in the current location.
- `mv <file-name> <dir-path>` - Move a file from one dir to another.
- `mv <file-name> <new-fie-name>` - Rename a file.
- `mv -R <dir-name> <dir-path>` - Move Dir
- `rm <file-name>` - Remove a file permanently.
- `rm -R <file-name>` - Delete a folder with dir included.
- `head <file-name>` - Will display first 10 lines of a file.
- `tail <file-name>` - Will display last 10 lines of a file.
    -`-n 2` - will display last 2 lines.
- `diff <file-1> <file-2>` - Show diff between the two files.
- `locate <file>` - To find out the file.  
- `find <file/folder-name>` - Find a file/folder.
- `find <dir-name>` - Find files inside the dir
- `find .-type d` - Show only dir.
    - `.-type f` - show only files.
    - `.-type f -name "*.txt"` - Show only files with that specific name.
    - `.-type f -iname "*.txt"` - Show only files with that specific name - not case sensitive (i)
    - `.-type f -mmin -20` - Show files which modify less than 20 min ago.
    - `.-type f -mmin +20` - show files which modify more than 20 min ago.
    - `.-type f -maxdepth 2` - Will only show 1 folder deep.
    - `.-size +1k` - will only show file/folder with size of 1kb


### System commands
- `ps aux` - processes which are running
- `systemctl [option] [service]` - interact with a process
    - We can do 4 `option` with `systemctl`
        - start
        - stop
        - enable
        - disable
    - Example, `systemctl start apache2`     
- `df` - Check the capacity and storage details.
    - `m` - In megabyte  or 
    - `hg` - In gigabyte.
- `du` - Disk usages capcity 
    - `-h` (human readable)
- `echo` - Get a output of a string
- `echo $PATH` - Check the path variable
- `sudo` - Admin command
- `sudo chown root text.txt` - change owner
- `!<command-name>` - Run the previous command
- `git add .; git commit -m "message"` - Run multiple commands at a time
- `sort <file-name>"` - sort the file
- `job` - show the jobs
- `wget <url>` - download the file from the URL
- `top` - what processes are running
- `kill <process-id>` -stop that process
- `Uname` - show the system info
- `zip <file-1> <file-2>` - Zip Two or more files
- `Unzip <file-name>` - Unzip files
- `useradd <name>` - add a user
- `passwd <name>` - set a password for the user
- `uname -<flag>` -o -m -r
- `lscpu` - get cpu details
- `free` - free memory 
- `vmstat` - virtual memory
- `lsof` - list all the open file
- `xdg-open <file-fath>` - open the folder (graphical window) of a file/folder with path.
- `xdg-open .` - open the folder of the current directory.
- `vi ~/.bashrc` - set your Alias
- `echo -n 'username' | base64` - encode the username to base64
- `echo -n 'encoded' | base64 -d` - decode the username to base64

### Networking
- `nslookup google.com` - To check the IP address of the domain.
- `netstat` - To check the network status.
- `hostname` - To check the hostname.
- `whoami` -  To check the current user.
- `ping google.com` - To check the connectivity.


### Permissions
- `chmod u=rwx,g=rxw,o=rwx <file-name>` READ, WRITE AND EXECUTE
- `chmod 777 <file-name>` - 4- Read, 2- Write, 1 - Execute
- `find . -perm 777 ` - shows files with all permissions(rwx)
- `grep <keyword> <file-name>` - To search if the keyword is presnt in the file or not
- `grep -w <keyword> <file-name>` - To search if the keyword is present in the file or not (complete word)
- `grep -i <keyword> <file-name>` - To search if the keyword is present in the file or not (not case sens)
- `grep -n <keyword> <file-name>` - To search if the keyword is present in the file or not (Line number)
- `grep -B <keyword> <file-name>` - Show Line before that keyword
- `grep -win <keyword> ./*.txt` - To search if the keyword is present in the file in current dir
- `grep -win -r <keyword> .*` 
- `history | grep "ls -l"` - Piping, we filter out the things

```
history
!<number-from-history>
```

# Operators

- `ping google.com & ping facebook.com` - run both the commands at the same time
- `echo "google.com" && echo "facebook.com"` - second will only run if first is successful
- `echo "google.com" && {echo "facebook.com"; eco "pradumnasaraf.co"}` 
- `echo "google.com" || echo "pingfacebook.com"` - second will only run if first is not successful
- `rm -r !(file.txt)` - delete all files except file.txt
- `printevnv` - to print all th env.



