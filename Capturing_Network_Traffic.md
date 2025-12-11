<h1> Capturing Network Traffic</h1>

<h2>Filter Traffic on Wireshark</h2>
<p>I chose to searfch for the string "card", since the lab is asking to find credit card information</p>
<img width="2557" height="148" alt="Screenshot 2025-12-11 120716" src="https://github.com/user-attachments/assets/c774bd5b-8bd9-4f89-abb0-19b9114d60b4" />
<br> 
<br>
<h2>Credential Hunting</h2>
<p>I found a GET request to /card , but it recieved a 404 error code. This means I need to keep looking</p>
<img width="2505" height="169" alt="Screenshot 2025-12-11 120723" src="https://github.com/user-attachments/assets/8c0a4ffd-7d36-453e-a1d1-96f153057909" />

<br>
<br>

<p>I found a successful GET request to /cart after scrolling down. It received a 200 OK code</p>
<p>Lets check out the packet contents of the 200 OK packet</p>
<img width="2505" height="204" alt="Screenshot 2025-12-11 120748" src="https://github.com/user-attachments/assets/088d10ac-3be7-4a8d-8639-8b431e76264c" />
<br>
<pr>Here we can see a form which sends a POST to /process_payment</pr>
<img width="1223" height="463" alt="Screenshot 2025-12-11 120840" src="https://github.com/user-attachments/assets/0c864fef-542b-47fd-9e2a-380d3602af5f" />
<br>
<p>Now, I will be filtering to look for the string "/process_payment"</p>
<p>It looks like we found a successful POST request, which received a successful 200 OK</p>
<img width="2501" height="220" alt="Screenshot 2025-12-11 120908" src="https://github.com/user-attachments/assets/878c34a3-fe29-45ff-a858-707f76fb72b6" />
<p>Lets check out whats inside this packet</p>
<br>
<h2>Credentials Found</h2>
<p>It looks like we have found credit card information in the /process_payment POST request packet</p>
<img width="1268" height="556" alt="Screenshot 2025-12-11 120918" src="https://github.com/user-attachments/assets/8a8e23c1-809f-4e0a-8d58-1285b6f6984e" />

<h3>Easier Method</h3>
<p>After completing the lab, I simply filtered to look for POST requests</p>
<img width="2556" height="1298" alt="Screenshot 2025-12-11 121750" src="https://github.com/user-attachments/assets/3982262c-c47a-4477-8c9f-06e8a9b50fcd" />

<br>
<h3>Capturing FTP data</h3>
<p>We can see at the very bottom of the packet that creds.txt is being transferred</p>
<img width="2531" height="1276" alt="Screenshot 2025-12-11 121913" src="https://github.com/user-attachments/assets/283b4742-6651-44c0-b367-b5b10f8ce50c" />
<br>
<p>We can see in the next FTP data packet that the username and password is in cleartext</p>
<img width="2117" height="1258" alt="Screenshot 2025-12-11 121927" src="https://github.com/user-attachments/assets/569ce0c2-997a-42e0-964a-26e8b0786887" />

<h2>Conclusion</h2>
<p>This lab shows the flaw with using unencrypted methods for network traffic, and shows how easy it can make a man in the middle attack</p>

