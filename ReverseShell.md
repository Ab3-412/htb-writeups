# Reverse Shell HTB Module Writeup 
This module explained what a Reverse Shell is and how to set one up 
<hr>

# Step 1 - Set up listener on attack machine 
(use common port to avoid outbound traffic being blocked by firewalls)
<img width="1262" height="160" alt="Screenshot 2025-09-04 180602" src="https://github.com/user-attachments/assets/921950ff-aabf-4634-89ca-b7e55779801d" />

# Step 2 - RDP Into Windows Target Sysetm 
(credentials were given for this module)
<img width="1227" height="98" alt="Screenshot 2025-09-04 180629" src="https://github.com/user-attachments/assets/7996c386-0346-4c7c-8d4d-8870d9083a32" />
<br>
<img width="600" height="auto" alt="Screenshot 2025-09-04 180737" src="https://github.com/user-attachments/assets/22257ae3-80e2-4955-8f42-e342a92b23c3" />

# Step 3 - Create Reverse Shell in Command Prompt on Target Device 
make sure to run this command in command prompt instead of powershell, it took me a second to realize I was in the wrong environment 
<img width="1014" height="181" alt="Screenshot 2025-09-04 183521" src="https://github.com/user-attachments/assets/9e9305cd-5438-45fd-b8a3-dabd15fc7df3" />

# Step 4 - Access the Target from Attack Box
<img width="1043" height="200" alt="Screenshot 2025-09-04 183537" src="https://github.com/user-attachments/assets/f72871f7-5ec9-4d7b-bc04-95166489c2e4" />


