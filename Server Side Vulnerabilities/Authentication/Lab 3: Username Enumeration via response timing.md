## Lab: Username enumeration via response timing

This lab is vulnerable to username enumeration using its response times. To solve the lab, enumerate a valid username, brute-force this user's password, then access their account page. 

    Your credentials: wiener:peter
-    Candidate usernames
-    Candidate passwords

End Goal: Enumerate a valid username and password and exploit the target 

## Steps 

1. first try to login with random user test | response -> [You have made too many incorrect login attempts. Please try again in 30 minute(s).]


2. second try to login with known password -> peter | response -> the same above 

3. add X-Forwarded-for: header to the request | response -> invalid username or password. so the response changed

4. now try to brute force the username and the X-Forwarded-For with pitchfork attack type 
| first list Numbers from 5 to 105
| second list Usernames list
-> Looking for different response time
found a valid username [ auto ]

5. now brute force the password with the provided list and X-Forwarded-For with two lists
-> Looking for 302 status code
found a valid password [ 2000 ]

creds: auto:2000
take the response url from burpsuite and search it in the browser [ finally u have logged in ]

