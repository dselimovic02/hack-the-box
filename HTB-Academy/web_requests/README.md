# Description

This document contains solutions for all questions from Web Requests module.

# HTTP Fundamentals
## HyperText Transfer Protocol (HTTP)

Our task here is to download /download.php file using cURL.

After starting our target machine we input the following command:

`curl -O <TARGET_IP>/download.php`

We use the `-O` option when we want to keep the remote file name.

Replace `<TARGET_IP>` with the IP address of your target machine.

![image](screenshots/output.png)

Next, we run `ls` command to list the contents of our current directory.

![image](screenshots/list.png)

We can see that we have downloaded the file sucessfully.
Now we just need to read the contents of our file. We can do that using the `cat` command: 

![image](screenshots/flag.png)

