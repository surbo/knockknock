**How to check if your recipient is using a FireEye mail product inline.**
Prerequisites: Python and SimpleHTTPServer 1)Stand up an internet facing server or cloud server. Shameless plug https://www.linode.com/?r=77675824b7701f904adb8404244f13d2c04cfc89
2)Open port 8080 or some other port that is not in use.
3)Open SimpleHTTPServer via terminal by typing python -m SimpleHTTPServer 8080
4)Send an email to the recipient with the following  http://x.x.x.x:8080/VerifyAccount/bob@1.com/data
  Note: You will need to swap in your IP address for the x.x.x.x and you can choose to leave bob@1.com or replace it with your recipient email address.
5)Once the email as been sent, you will see a 404 response within the terminal. If the email address has been replaced with nobody@mycraftmail.com after the VerifyAccount/ you know they are using FireEye inline.This works as of 2/19/2020 
