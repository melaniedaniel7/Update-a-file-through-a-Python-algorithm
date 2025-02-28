# Algorithm for file updates in Python
Disclaimer: This project was created as part of my learning journey through the Google Professional Cybersecurity Certificate offered on Coursera. Some activities and content within this project were provided by the course as part of my coursework. All credit for such content belongs to Google and Coursera, and I acknowledge their role in supporting the completion of this project.

### Project description
In this scenario I was a security analyst at a health care company. The company has a file that
only authorized employees can access. The authorized employees are identified by their IP addresses
and it is my job to keep this file up to date. I use a Python algorithm to keep this file up-to-date
and automate the process of parsing the file.

The algorithm I have developed parses the text file of IP addresses and updates the file by removing 
IP addresses that no longer have access to the restricted content.

Parsing a file allows security analysts to read and update the contents. 
Parsing is the process of converting data into a more readable format.
An important part of cybersecurity and my job as a security professional 
is controlling access to restricted content.

Below are the steps I followed to create this algorithm.

### Open the file that contains the allow list
The file that I want to open is called `"allow_list.txt"`. 
I start by assigning a string containing this file name to the `import_file` variable. 
Then, I use a `with` statement to open it.
The keyword `with` handles errors and manages external resources. 
The `open()` function opens a file in Python.
I use the variable `file` to store the file while I work with it inside the `with` statement.
The purpose of opening the file is to allow me to access the IP addresses stored in the allow list file.

💡 `"r"` indicates that I want to read the file.

💡 The `as` keyword assigns a variable that references another object. When you open a file using `with open()`, you must provide a variable that can store the file while you are within the `with` statement. You can do this through the keyword `as` followed by this variable name. 

<img src="Screenshot 2025-02-23 at 17.40.45.png" width="600" />

### Read the file contents
Next, I use the `.read()` method to convert the contents of the allow list file into a string so that I can read them.
The `.read()` method converts files into strings. 
This is necessary in order to use and display the contents of the file that was read.
I store this string in a variable called `ip_addresses`.
This code reads the contents of the `allow_list.txt` file in a string format
that allows me to later use the string to organize and extract data in my Python program.

<img src="Screenshot 2025-02-23 at 18.48.00.png" width="600" />

### Convert the string into a list
In order to remove individual IP addresses from the allow list, the IP addresses need to be in a list format. 
Therefore, I use the `.split()` method to convert the `ip_addresses` string into a list.
The `.split()` method converts a string into a list. It separates the string based on a specified character that's passed into `.split()` as an argument. 
The purpose of spliting `ip_addresses` into a list is to make it easier to remove IP addresses from the allow list.
To store the list I reassigned it back to the variable `ip_addresses`.

<img src="Screenshot 2025-02-23 at 19.01.23.png" width="600" />

### Iterate through the remove list
A second list called `remove_list` contains all of the IP addresses that should be removed from the `ip_addresses` list. 
I set up the header of a `for` loop that will iterate through the `remove_list`. 
The `for` loop is an iterative statement that iterates through the IP addresses (in this scenario).
I use `element` as the loop variable and the keyword `in`.
The keyword `in` indicates to iterate through the sequence `ip_addresses` and assign each value to the loop variable element.

<img src="Screenshot 2025-02-23 at 19.05.06.png" width="600" />

### Remove IP addresses that are on the remove list
In the body of my iterative statement, I add code that will remove all the IP addresses from the allow list that are also on the remove list. 
First, I create a conditional that evaluates if the loop variable `element` is part of the `ip_addresses` list. 
Then, within that conditional, I apply the `.remove()` method to the `ip_addresses` list and remove the IP addresses identified in the loop variable `element`.
The `.remove()` method is used to remove an element, which in this case is an IP address from the `remove_list`.
💡Applying the .remove() method in this way is possible because there are no duplicates in the ip_addresses list.

<img src="Screenshot 2025-02-23 at 19.15.51.png" width="600" />

### Update the file with the revised list of IP addresses
Now that I have removed these IP addresses from the `ip_address` variable, I can complete the algorithm by updating the file with this revised list. 
To do this, I must first convert the `ip_addresses` list back into a string using the `.join()` method. 
I apply `.join()` and `"\n"`to the string in order to separate the elements in the file by placing them on a new line.
The `.join()` method concatenates the elements of an iterable into a string. 
Put simply, this means that it converts a list back into a string.
Then, I used another `with` statement and the `.write()` method to write over the file assigned to the `import_file` variable.
This way, the restricted content will no longer be accessible to any IP addresses that were removed from the allow list.
The `.write()` method writes string data to a specified file. 
💡You should use the `"w"` argument when you want to replace the contents of an existing file.

<img src="Screenshot 2025-02-23 at 19.21.21.png" width="600" />
<img src="Screenshot 2025-02-23 at 19.21.55.png" width="600" />

### Summary
In this scenario I created an algorithm that removes unauthorized IP addresses identied in a `remove_list` variable from the `"allow_list.txt"` file of approved IP addresses.
The algorithm opened the file, converting it to a string to be read, and then converting this string to a list stored in the variable `ip_addresses`. 
I then iterated through the IP addresses in `remove_list` with a `for` loop.
With each iteration, I evaluated if the element was part of the `ip_addresses` list. If it was, I applied the `.remove()` method to it to remove the element from `ip_addresses`. 
Finally, I used the `.join()` method to convert the `ip_addresses` back into a string so that I could write over the contents of the `"allow_list.txt"` file with the revised list of IP addresses.

