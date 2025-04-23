# Input Validation Mechanisms

[](https://rkive.gitbook.io/~gitbook/image?url=https%3A%2F%2F3577347090-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FWrIcinZ87qSasUAtuqcU%252Fuploads%252FM3bPwVIWXsf7ZCVD2dNS%252Fimage.png%3Falt%3Dmedia%26token%3D630fa778-398a-4468-bb47-0a0189092a37&width=768&dpr=4&quality=100&sign=aab32c74&sv=2)

# Input Validation

> **Input validation** is something that is used to limit the user input for attaining just the required functionality through input testing. Since some of the vulnerabilities like XSS, SQL Injection, SSTI, etc. are possible due to lack of implementation within input validation, it is necessary to understand what we are able to implement to prevent these vulnerabilities and prevent any of the **Confidentiality**, **Integrity**, and **Availability** issues. Since different programming languages offer different methods to validate the input, the mechanism of either **whitelisting** or **blacklisting** remains the same for all languages.
> 

The validation must be done within both the **Syntactical** and **Semantic** Levels.

# Syntactical Level

***Syntactical Level**:* From the name, we are able to guess that the syntactical is related to the syntax of any input. Hence, the syntax of the structured fields needs to be validated.

**For example:**

- ***Phone Number**:* +9779812345678, which shows that we have a + symbol at the beginning of the syntax followed by a country code that could be between 1 to 3 in length along with the phone number, 10 in length allowing only digits from 0 to 9.

# Semantic Level

***Semantic Level:*** Semantics comes to play when the correctness of the values is within the required context. For example: Dates: Allowing dates with limits where required. If a date for a user’s enrollment within a university is given, the semantic validation should not allow the user to enter any dates before the enrollment date for graduation.

Implementation of input validation Some of the new developers working without frameworks usually only handle the validation on the frontend part making the application vulnerable when the requests are modified through different tools like Burp Suite or even the browser’s ability to modify and resend requests.

Hence, validation should be done for both the front end and the back end. But most of the input validation is already available in frameworks such as Django which gives the developers ease in implementing these validations. But some of the validation needs to be done according to the cases we see.

**The following are the ways to set validations:**

- Checks for specific schemas such as JSON, XML, etc., and including strict checks for validation.
- Using exception handling to handle special cases and using data types to specify the type of data being input rather than using strings for every data type.
- The range of the characters should be checked and limited so that no more than the specified range can be input.
- Using regular expressions must be done to cover the whole string rather than just sections of the string i.e. using the ^ to scan from the starting of the string and $ till the end to make sure the whole string is selected rather than a substring involved.
- Only allow a set of required characters to be accepted
- Using encoding to encode special characters that need to be output to the page or application
- Validate the same set of rules for the name of the uploads for the files and rename them randomly using UUIDs or any naming convention that is very random.
- Validate the size of the uploaded file and the extension of the file. The extension of the file must be validated and limited.
- For files that are zipped and uncompressed later by the server, validation of the zip needs to be done beforehand which includes the target path, level of compression, and the estimated size of the decompressed file.
- The uploaded files need to be scanned for any malicious content and need to be verified.
- The file path of the file must be set from the server side (backend) not the client side (frontend)
- The content type of the uploaded file must be predefined and served accordingly Executable scripts, configuration files, and other cross-domain config files must be blocked from uploading.
- Using image rewriting libraries to verify the validity of the image and removal of excess content should be done. The image must be set to be of certain formats only. Some feel that stopping the extension of the file would be a good solution but the content of the image needs to be checked beforehand as there are executable scripts that can be renamed and uploaded.
- Strict email address validation needs to be done from the client side as well as the server side. [https://tools.ietf.org/html/rfc5321#section-4.1.2](https://tools.ietf.org/html/rfc5321#section-4.1.2) defines the format of the email addresses. Using regex to have syntactic validation and using techniques to verify through semantic validation that the email actually exists is a way to validate emails.
- Blacklisting email addresses that are disposable could be a solution but since domains can be created and creating a mail server is very easy, the process to blacklist could be endless. So, whitelisting of email addresses could be done wherever possible.

Hence by following the above methods to whitelist and blacklist a set of syntactic rules and following some semantic procedures, we are able to validate data that has been input.

# **What to Do When Input Fails Validation?**

So, what do you do when input fails validation? There are two major approaches: **recovering** and continuing on, or **failing** the action and reporting an error. Each has its advantages and disadvantages:

- ***Recovering:*** Recovering from an input validation failure implies that the input can be sanitized or fixed — that is, that the problem that caused the failure can be solved programmatically. This is generally more likely to be possible if you are taking a blacklisting approach for input validation, and it commonly takes the approach of removing bad characters from the input. The major disadvantage of this approach is ensuring that the filtering or removal of values does actually sanitize the input, and doesn’t just mask the [malicious input](https://www.sciencedirect.com/topics/computer-science/malicious-input), which can still lead to SQL injection issues.
- ***Failing:*** Failing the action entails generating a security error, and possibly redirecting to a generic error page indicating to the user that the application had a problem and cannot continue. This is generally the safer option, but you should still be careful to make sure that no information regarding the specific error is presented to the user, as this could be useful to an attacker to determine what is being validated for in the input. The major disadvantage of this approach is that the [user experience](https://www.sciencedirect.com/topics/computer-science/user-experience) is interrupted and any transaction in progress may be lost. You can mitigate this by additionally performing input validation at the client’s browser, to ensure that genuine users should not submit invalid data, but you cannot rely on this as a control because a malicious user can change what is ultimately submitted to the site.

Whichever approach you choose, ensure that you log that an input validation error has occurred in your application logs. This could be a valuable resource for you to use to investigate an actual or attempted break-in to your application.
