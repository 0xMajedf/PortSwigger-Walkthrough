## Username Enumeration
is when an attacker is able to observe changes in the website's behavior in order to identify whether a given useranme is valid
Username enumeration typically occurs either on the login page, for example, when you enter a valid username but an incorrect password, or on registration forms when you enter a username that is already taken. This greatly reduces the time and effort required to brute-force a login because the attacker is able to quickly generate a shortlist of valid usernames

##  While attempting to brute-force a login page, you should pay particular attention to any differences in: 
- Status codes
- Error Messages
- Responses Times

## Lab: Username enumeration via different responses
This lab is vulnerable to username enumeration and password brute-force attacks. It has an account with a predictable username and password, which can be found in the following wordlists: 

End Goal: Find the correct username and able to brute force the password correctly and login to the account

provided wordlists
- Candidate usernames
- Candidate passwords

Steps:
1. first check the reponse by entering random username with test -> Invalid username

2. after checking the response try to brute force the username parameter to be able to find a valid username first using ffuf or burpsuite pro or any other fuzzing tool 

3. after brute forcing the username paramter found a valid username with a different respone -> incorrect password 

4. now start brute forcing the password paramter -> 302 Found
- Creds: auto:abc123

5. Login to the account