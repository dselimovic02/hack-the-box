# Description

This document contains solutions for all questions from Web Requests module.

# HTTP Fundamentals
## HyperText Transfer Protocol (HTTP)

Our task here is to download /download.php file using cURL.

After starting our target machine we input the following command:

`curl -O <TARGET_IP>/download.php`

We use the `-O` option when we want to keep the remote file name.

Replace `<TARGET_IP>` with the IP address of your target machine.

![image](screenshots/http_1.png)

Next, we run `ls` command to list the contents of our current directory.

![image](screenshots/http_2.png)

We can see that we have downloaded the file sucessfully.
Now we just need to read the contents of our file. We can do that using the `cat` command: 

![image](screenshots/http_3.png)

## HTTP Requests and Responses

We have two tasks here:
  1. Find out what is the HTTP method used while intercepting the request. (case-sensitive)
  2. Find out the version of Apache server running on our target.

We can find out all of the needed information by running one single command:

`curl <TARGET_IP> -v`

Replace `<TARGET_IP>` with the IP address of your target machine.

By using `-v`, verbose,  option we will get both request and response in our output.

![image](screenshots/requests_and_responses.png)

Line `> GET / HTTP/1.1` is the soultion to our first question. HTTP method used is GET.
Line `< Server: Apache/2.4.41 (Ubuntu)` gives us the version of Apache server which is 2.4.41

## HTTP Headers

This time we are tasked to use browser dev tools instead of cURL.

  1. Search for the target, with its IP address, inside your browser of choice.
  2. Open brower dev tools [ctrl + shift + i].
  3. Open Network tab.
  4. Refresh [ctrl + r].
  5. Select file with name flag...
  6. Open response tab and copy the flag.

  ![image](screenshots/headers.png)

  # HTTP METHODS
  ## GET

For this task we need to log in our target with supplied user credentials via browser.
Credentials are 'admin' for username and same for password.

 ![image](screenshots/get_1.png)

 After we gain access to the website, we need to search for any term using the search box provided.

 ![image](screenshots/get_2.png)

 The output is not that interesting. Now we need to find out the method that was used for data retrieval. We can find that info in the Network tab of the dev tools.
 We go to our Network tab of dev tools and refresh using [ctrl + r]. Then we search again for any term.

 ![image](screenshot/get_3.png)

After finding out the call and method, we can get our flag by searching for that term with cURL.

![image](screenshots/get_4.png)
