#### Introduction :
#### I -[Authentication](#Authentication ) 
#### II - [Injection](#Injection)
#### III- [Toxic Dependencies](#Toxic_Dependencies) 
#### IV- [Insecure Design](#Insecure_Design)
#### V- [Dns Configuration](#DNS_configuration)
#### VI- [HTTPS Enforcement](#HTTPS_enforcement)
#### VII- [Access Control](#Access_Control)
#### VIII- [Encrypted Communication](#Encrypted_Communication)
#### IX- [Denial Of Service](#Denial_Of_Service)

### Authentication 
[[Authentication security]] Is no joke .
we can add different layers of it :
1. [[password mismanagement]] + [[user enumeration]]: managing password in two ways : 
	1. integrating third party Password managers such as Aauth , OpenID , SAML
	2. Capcha
	3. Password management by forcing the user to strong passwords
	4. encryption of password on database by Bcrypt + salt + pepper of the password
	5. if The user writes wrong password or email : don't show them wrong password or wrong email but more of : wrong email or password
	6. Password reset email : time out after 5 minutes 
	7. write old password to change the current password 
	8. password lockout after 10 attempts
	9. inspiration by Discord security system in login 
	10. Never commit any default login details or sensitive API credentials to your code repository. Maintain these settings in the `.env` file in the project root.
	11. hey should be sent over HTTPS only and never display in your application. The `secure` setting can be enabled in the `session.php` config file of your Laravel application.
	12. Rerourceez :https://github.com/antonioribeiro/google2fa /
2. [[privelage escalation]] : 
	1. only the **session ID** is passed back and forth between client and server, and all session-related data is kept on the server.
	2. Session state has to be persisted and looked up with each HTTP request.
	3. encrypt each single request : overheat .
3. [[session fixation]] + [[weak session ids]] :
	1. regeneration of session IDs each time the user logs in 
	2. Timeout and Replace Old Session IDs
	3. implement strong logout function 
	4. Require a New Session When Visiting From Suspicious Referrers
	5. [[session]] : laravel section for sessions (documentation)
	6. https://php.net/manual/en/function.session-regenerate-id.php : tracked with cookies 
	7. for weak session ids [[weak session ids]] 
	
### Injection
[[sql injection]] : 
1. Using best practices in : postgresql , php , nodejs
2. https://www.invicti.com/blog/web-security/sql-injection-cheat-sheet/?utm_source=hacksplaining&utm_medium=post&utm_campaign=articlelink
3. Oauth helps on this as well !!
[[XSS Injection ]] : 
1. Not studied yet
[[host header poisonning]] : 
1. Not studied yet

### Toxic_Dependencies
Being aware of toxic  dependencies and trying to avoid them : 
1. Keeping them all uptodate
	1. https://github.blog/2020-06-01-keep-all-your-packages-up-to-date-with-dependabot/
2. [https://retirejs.github.io/retire.js/](https://retirejs.github.io/retire.js/)
3. [https://docs.npmjs.com/auditing-package-dependencies-for-security-vulnerabilities](https://docs.npmjs.com/auditing-package-dependencies-for-security-vulnerabilities)
4. keep it clean , No shady dependencies 




### Insecure_Design 
1. Apply Stride Model  which is the most [[insecure design]]
2. having one source control (git ) so we can analyze code changes for potential security flaws
3. Github actions and automation 
4. manage dependecies and packages automatically 
5. Unit testing along the way 
6. code reviews along the way to spot potential vulnerabilities 
7. I feel like the teacher likes Using systems , it would be beneficial to apply stride model 
8. code fails securely : to not leak any internal architectural details in error messages 

	[[Information Leakage]] : 
		1. do not leak infos  in the interface (check the link above in information leakage)

### DNS_configuration 
1. check this : [[dns poisoning]]
2. use DNSSEC
3. [dns cache poisoning ](https://www.cloudflare.com/en-gb/learning/dns/dns-cache-poisoning/)
### HTTPs_enforcement  
[[ssl stripting]]
[[cross site scripting]]

### Access_Control 
[[Broken Acces Control]]
[[Directory Traversal]]
[[cross-site request forgery]]

### Encrypted_Communication 
	[[unencrypted communication]]
	1. use let's encrypt 
	2. Reverse Proxies
### Denial_Of_Service 
1. Be aware of [[regex injection]]
2. Be aware of [[buffer overflows]]
3. 

