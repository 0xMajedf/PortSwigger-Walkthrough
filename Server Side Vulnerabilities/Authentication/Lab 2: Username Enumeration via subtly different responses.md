This lab is subtly vulnerable to username enumeration and password brute-force attacks. It has an account with a predictable username and password, which can be found in the following wordlists: 

-    Candidate usernames
-    Candidate passwords

End Goal: Find the correct username and password and login to the account 
## Steps:

1. check for the response code by entering a random username like test  -> Invalid username or password.

2. brute force the username paramter with the provided wordlist

3. after brute forcing username paramter and clicking on the length or the status code it appears all the requests have the same answer -> Invalid username or password. to solve this issue u could filter by negative search [ Invalid username or password. ] -> found a user with different response Invalid username or password [ without a .] ... username: albuquerque

4. after identifying a valid username by filtering the response code now start brute forcing the password paramter with the provided wordlist -> 302 Found
- creds: albuquerque:ranger

5. Login to the account

