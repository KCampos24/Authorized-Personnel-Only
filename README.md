<h1>File Parsing to Maintain Secure Access Control</h1>

<h2>Project Description</h2>
<p>
    This project showcases how Python can be used to efficiently manage and update files. Specifically, it involves updating a file that controls employees access to sensitive information, ensuring that only authorized personnel have access to the most current records.
</p>

<h2>Open the File that Contains the Allow List</h2>
<p>
  <p align="center">
<img src="https://i.imgur.com/sdqKO9P.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
    A text file called <code>allow_list.txt</code> contains a list of IP addresses that are allowed to access restricted information. A separate remove list is provided to specify which IPs should be removed from the allow list. The Python <code>with</code> statement and <code>open()</code> function are used to safely open and close the file. The first argument within the function is the name of the file, and the second is the mode in which the file is opened. <code>as</code> will be used to assign the file to a variable in this case named file.
</p>

<h2>Read the File Contents</h2>
<p>
  <p align="center">
<img src="https://i.imgur.com/5AsL96h.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
    The contents of the file are read and stored as a string using the <code>.read()</code> method. The string is assigned to the <code>ip_addresses</code> variable.
</p>

<h2>Convert the String into a List</h2>
<p>
  <p align="center">
<img src="https://i.imgur.com/ufpSQYM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
    To remove IP addresses, the string must be converted into a list. The <code>.split()</code> function splits the string into individual elements, which are stored in a list.
</p>

<h2>Iterate Through the Remove List</h2>
<p>
  <p align="center">
<img src="https://i.imgur.com/SXecMq8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
    A <code>for</code> loop is used to iterate through the <code>remove_list</code>, checking each IP address to see if it needs to be removed from the <code>ip_addresses</code> list.
</p>

<h2>Remove IP Addresses from the Allow List</h2>
<p>
  <p align="center">
<img src="https://i.imgur.com/jMKemoa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
    Inside the loop, the <code>.remove()</code> function is called to remove any matching IP addresses from the allow list. Since there are no duplicate IP addresses, the <code>.remove()</code> method is safe to use.
</p>

<h2>Update the File with the Revised IP List</h2>
<p>
  <p align="center">
<img src="https://i.imgur.com/w8IgCNk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
    After modifying the list, the <code>.join()</code> method is used to convert the list back into a string. The file is then opened in write mode (<code>"w"</code>), and the updated string is written back to the file, overwriting the old contents.
</p>

<h2>Summary</h2>
<p> This Python algorithm highlights the critical role of file parsing in maintaining secure access control. By using essential functions like <code>open()</code>, <code>.split()</code>, and <code>.join()</code>, it efficiently manages and updates sensitive files. In cybersecurity, ensuring files are accurately modified and up-to-date is vital for controlling access and safeguarding confidential information.
</p>
