# Phishing---Merry-Clickmas---tryhackme
# Scenario
- In light of several recent cyber security threats against The Best Festival Company (TBFC), the local red team has scheduled several penetration tests. The red teamers proceeded to carry out a regular penetration test against their TBFC. Part of this exercise is to ensure that the employees are diligent when clicking links and that the company is well protected against the latest phishing attacks. This type of authorised phishing is a proven way to learn whether the cyber security awareness training has fruited.
# Tools used
- Social-Engineer Toolkit
- Python (http server)
- Terminal
- Firefox Web Browser
# Solve steps
1.  After I started the attacker machine I opened the terminal and went to /Rooms/AoC2025/Day02 using "cd Rooms/AoC2025/Day02" where the installed script server.py can be exploited
2.  Typed "./server.py" to start the script and listen on my local IP address on port 8000
3.  On another terminal I used the toolkit to create a Social Engineering email by typing "setoolkit":
-  (1) ---> Social-Engineering Attacks
-  (5) ---> Mass Mailer Attack
-  (1) ---> E-Mail Attack Single Email Address
4. Now there is some questions I will type the answers I used:
------------------------------------------------
- **Email subject:** "Shipping Schedule Changes"
- **Send the message as HTML or plain:** I pressed enter for plaintext (the default)
- **Enter the body of the message, and type END (capitals) when finished:** Here typed so words to make the victim click the link (the server.py IP)
- **Send email to:** factory@wareville.thm
- **How to deliver the email:** (2) ---> Use your own server or open relay
- **From address:** updates@flyingdeer.thm
- **From name:** Flying Deer
- **Username for open-relay:** Enter (the default)
- **Password for open-relay:** Enter (the default)
- **SMTP email server address:** 10.114.184.54
- **Port number for the SMTP server:** Enter (the default)
- **Flag this message as high priority:** no
- **Do you want to attach a file:** n
- **Do you want to attach an inline file:** n
###### That's all then press Enter
------------------------------------------------
5. In 1 or 2 minutes I had the username and the password
<img width="787" height="97" alt="Screenshot 2026-08-23 19352 2" src="https://github.com/user-attachments/assets/cf8ca954-d93a-470e-8256-346b3efacac9" />

6.  Now I had to know if the admin used this password anywhere else so I went to http://10.114.184.54 in Firefox and tried the password on another user "factory" and it worked 
<img width="1914" height="383" alt="Screenshot 2026-08-23 19441" src="https://github.com/user-attachments/assets/f1e38f95-3312-4dfd-8c50-0a2e647c8437" />

7. Here I was able to see the total number of toys expected for delivery and it was the last question
