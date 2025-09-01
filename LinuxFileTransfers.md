#Linux File Transfers HTB Module 

This module focuses on being able to download and upload files from one machine to another. The lab also challenges you by limiting the environment you ssh into, which I will show how I still executed the desired commands 

#Step 1 - Upload File to Target Machine
In the HTB module, the lab asks for you to upload a given zip file named "upload_nix.zip" to the target machine
*The Username/IP/Password were all given for this exercise*
The method I chose for uploading my file was SCP, which is shown in the screenshot below:
<img width="707" height="172" alt="Screenshot 2025-09-01 120758" src="https://github.com/user-attachments/assets/08bf33d1-1e8f-4f4a-85aa-d3dffa23979e" />

#Step 2 - SSH into Target Machine
Now that the file was uploaded successfully, I can now ssh into the target machine and see my uploaded file:
<img width="1243" height="772" alt="Screenshot 2025-09-01 120932" src="https://github.com/user-attachments/assets/764d03c8-1d31-4014-9c54-4e042dc982fe" />


#Step 3 - Unzip File (Challenge Solved)
It wouldn't be an HTB module without adding an extra challenge.
Here you can see that I am not allowed to unzip my uploaded file becuae I do not have "unzip" installed. I do not want to talk to an admin of course, so I will see if I can run an unzip command using another method.
<img width="639" height="142" alt="Screenshot 2025-09-01 124022" src="https://github.com/user-attachments/assets/f3e767c6-377a-41fa-93c0-f06983476119" />

You can run commands on your machine without needing to install it on your device. This can bypass certain permissions if you find yourself unable to download needed commands. 
In this instance, I checked to see if python was installed on the target machine:
<img width="654" height="34" alt="Screenshot 2025-09-01 124805" src="https://github.com/user-attachments/assets/0b513c57-97d9-402a-8e90-3122c8a8b505" />

With Python already installed, I can use an unzip function that is built into python without needing an external download 
<img width="959" height="52" alt="Screenshot 2025-09-01 124832" src="https://github.com/user-attachments/assets/50d49bd8-971a-4ff2-849e-c97e5549a115" />

I now go into my new extracted directory so I can run the given "hasher" command to view the hash of the file. 
<img width="1241" height="113" alt="Screenshot 2025-09-01 124847" src="https://github.com/user-attachments/assets/96ea0a2a-f30b-4ff4-8e75-f6575325a10f" />
And thats it, pretty simple module but it can take awhile if you don't know what to look for

#Bonus - Base64 encode/decode file transfer

I used cat to display the contents of my upload.nix.txt file, this will be used to later confirm a successful transfer (or more accurate, a successful copy)
<img width="532" height="45" alt="Screenshot 2025-09-01 125007" src="https://github.com/user-attachments/assets/e8cd1194-2515-49ef-be5f-5ed91b1a682a" />

I will now encode the file using base64 and display its contents, I will then copy this code and paste it into my desired linux machine 
<img width="1043" height="42" alt="Screenshot 2025-09-01 125001" src="https://github.com/user-attachments/assets/d5ce7531-f573-4e35-94da-dbe6dcd7b924" />

I paste the code into my machine by using echo and using a pipe to decode the base64 string, and outputting it back into an upload_nix.txt file
<img width="957" height="46" alt="Screenshot 2025-09-01 125034" src="https://github.com/user-attachments/assets/15e36a53-da8d-457b-bad8-995283cd2cfa" />

I can now display the contents of my new upload_nix.txt file and confirming that the contents remained the same between both machines
<img width="445" height="63" alt="Screenshot 2025-09-01 125048" src="https://github.com/user-attachments/assets/6382c772-4cf9-4e5e-aca8-8688a95231e5" />

This was just fun extra practice and shows another method of transfering file content
