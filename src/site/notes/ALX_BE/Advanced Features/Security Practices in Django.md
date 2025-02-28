---
{"dg-publish":true,"permalink":"/alx-be/advanced-features/security-practices-in-django/"}
---


https://docs.djangoproject.com/en/5.0/topics/security/

## Common Web Vulnerabilities and their Impact
- **<mark style="background: #FF5582A6;">Cross-Site Scripting (XSS)**:</mark>Attackers inject malicious scripts into web pages viewed by users. These scripts can steal sensitive data like cookies or login credentials, deface websites, or redirect users to phishing sites.
- <mark style="background: #FF5582A6;">**Cross-Site Request Forgery (CSRF)**:</mark> Malicious actors trick users into performing actions on a trusted website without their knowledge or consent. This can lead to unauthorised fund transfers, data modification, or account takeover.
- <mark style="background: #FF5582A6;">**SQL Injection**:</mark> Attackers manipulate database queries to gain unauthorised access to sensitive data, modify data, or even delete entire databases. This can have severe consequences, including data breaches and financial losses.
- <mark style="background: #FF5582A6;">**Clickjacking**:</mark> Users are deceived into clicking seemingly innocuous elements on a web page, while hidden elements perform unintended actions in the background. This can lead to the installation of malware, unauthorised purchases, or social media hijacking.
## Leveraging Django’s Built-in Security Features
- **<mark style="background: #BBFABBA6;">CSRF Protection</mark>**: Django’s CSRF middleware automatically generates and validates tokens for forms. This ensures that only forms originating from your own website can submit data, preventing CSRF attacks.
- **<mark style="background: #BBFABBA6;">XSS Protection</mark>**: Django templates automatically escape user-provided data by default. This process converts special characters into harmless entities, preventing malicious scripts from being executed in the browser.
- **<mark style="background: #BBFABBA6;">SQL Injection Protection:</mark>** Django’s querysets and ORM (Object-Relational Mapper) provide a secure way to interact with databases. They use parameterization to ensure that user input is treated as data, not executable code, preventing SQL injection attacks.
- **<mark style="background: #BBFABBA6;">Password Hashing</mark>**: Django stores passwords securely using robust hashing algorithms like PBKDF2 or Argon2. This makes it extremely difficult for attackers to crack passwords even if they gain access to the hashed password data.