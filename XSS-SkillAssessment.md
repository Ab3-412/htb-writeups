<h1> HTB XSS Skill Assessment</h1>

<h2>Find Vulnerable Field</h2>
<br>
<p>We can start a php listener which can be used to validate which field/s are vulnerable </p>
<img width="247" height="47" alt="listener" src="https://github.com/user-attachments/assets/c564858d-34d9-40d9-9a51-75b8ecb2ec68" />
<p>This can be done using payloads from the previous "Session Hijacking" section. The one that worked for me started with "> [script]</p>
<p>Use the "inspector" tool in the browser to find the field IDs</p>
<img width="719" height="844" alt="firstXss" src="https://github.com/user-attachments/assets/1bee9bf2-e6b9-447d-be14-de3744ad8371" />
<br>
<p>We can see that the "author" and "url" fields are vulnerable</p>
<img width="1287" height="164" alt="xssPOC" src="https://github.com/user-attachments/assets/f0a97c54-b57b-450c-809e-9dccd6c5b35a" />
<br>
<h3>Custom Script</h3>
<p>Use custom php script given in the "Session Hijacking" Module. This will be used to obtain the cookie</p>
<img width="1269" height="305" alt="givenScript" src="https://github.com/user-attachments/assets/dc56cd53-45cc-4e43-bb76-60d39a442a4f" />
<br>
<h3>Find Cookie Obtaining Payload</h3>
<p>Use trial and error with payloads from the "Session Hijacking" Module to find a working payload to obtain cookie</p>
<p>Instead of targeting a field's ID, we are targeting the custom script mentioned earlier (named index.php here)</p>
<img width="890" height="798" alt="finalXss" src="https://github.com/user-attachments/assets/aec051b4-806a-4a8a-a840-d14b2c02f7ab" />
<br>
<h3>Flag</h3>
<p>We can now see the flag</p>
<img width="1273" height="125" alt="flag" src="https://github.com/user-attachments/assets/631fe060-b3e8-445d-a5ef-50ea7f6ab18b" />

