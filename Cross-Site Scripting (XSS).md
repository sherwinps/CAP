# Cross-Site Scripting (XSS)

[](https://rkive.gitbook.io/~gitbook/image?url=https%3A%2F%2F3577347090-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FWrIcinZ87qSasUAtuqcU%252Fuploads%252FWzfZbcDrr64HS0MQuw7t%252Fimage.png%3Falt%3Dmedia%26token%3Df56f92b2-d8ca-409f-8573-2de5b5aa963d&width=768&dpr=4&quality=100&sign=84fcbeb5&sv=2)

# Cross-Site Scripting

> Cross-site scripting (XSS) is a type of security vulnerability typically found in web applications. It occurs when an attacker uses malicious code to inject a client-side script into a web page viewed by other users. This type of attack allows an attacker to manipulate how the web page is displayed for the viewer, and can potentially be used to gain access to user data or even inject malicious code into the web page itself.
> 

XSS attacks are typically carried out by injecting malicious code into the web page using HTML or JavaScript. This code can then be used to gain access to user data, alter the appearance of the page, or even send malicious commands to the server. The malicious code is often hidden in a URL, hidden form field, or in the HTML source of the web page.

XSS attacks are often used in conjunction with other attacks, such as phishing or malware, in order to gain access to user data or to execute malicious commands. They can also be used to spread malicious links or code to other users.

There are two main types of XSS:

# **Stored XSS**

In a stored XSS attack, the attacker injects malicious code into a website's database, where it is stored and executed whenever someone accesses a page that retrieves data from the database.

# **Reflected XSS**

In a reflected XSS attack, the attacker crafts a URL that includes the malicious code, and tricks a victim into clicking on it. When the victim's browser requests the URL, the server returns a page containing the injected code, which is then executed by the victim's browser.

# **Prevention**

There are several ways to prevent XSS attacks:

1. Input validation and sanitization: This involves checking user input for malicious content and removing or encoding it. This can be done on the client side using JavaScript, or on the server side.
2. Content Security Policy (CSP): CSP is a security feature that allows a website to specify which sources of content are allowed to be loaded by the browser. By using CSP, a website can prevent the execution of malicious code that has been injected into the website.
3. Escaping user input: This involves converting special characters in user input so that they are not interpreted as code. This can be done on the server side before the input is displayed on the website.
4. Encoding user input: This involves converting user input into a format that can be safely displayed on the website without being executed as code.
5. Disabling HTML in user input: This involves disabling the ability for users to input HTML tags and attributes in order to prevent the injection of malicious code.

It is important to note that no single solution can completely prevent XSS attacks, and a combination of these measures should be used to effectively mitigate the risk.