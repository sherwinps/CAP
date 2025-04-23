# Insecure File Uploads

[](https://rkive.gitbook.io/~gitbook/image?url=https%3A%2F%2F3577347090-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FWrIcinZ87qSasUAtuqcU%252Fuploads%252FwWhGgIeyGSi22rZeFZKi%252Fimage.png%3Falt%3Dmedia%26token%3D4c515365-9395-4c5e-9ef5-c57a0ee6b8a6&width=768&dpr=4&quality=100&sign=5365d3aa&sv=2)

# **Insecure File Uploads**

> File upload vulnerability is a common security issue found in web applications. Whenever the web server accepts a file without validating it or keeping any restriction, it is considered as an unrestricted file upload.
> 

# **Types of Insecure File Uploads**

There are several types of insecure file uploads, including:

- Unrestricted File Upload
- Insecure File Extensions
- Insecure Storage
- Unvalidated File Contents

# **Unrestricted File Upload**

Unrestricted file upload is a vulnerability that allows an attacker to upload malicious files to a web application. This can be done by exploiting the lack of authentication or authorization checks on the server-side of the application. Examples of this attack include uploading a malicious script or executable to a vulnerable web application.

# **Insecure File Extensions**

Insecure file extensions are file types that are vulnerable to attack. These include .exe, .vbs, .php and other types of scripts and executables. By allowing these types of files to be uploaded to a web application, the attacker can gain access to the application and its data.

# **Insecure Storage**

Insecure storage is where files uploaded to a web application are stored in an insecure location. For example, an attacker could upload a malicious file to a web application and then access the file from an insecure location.

# **Unvalidated File Contents**

Unvalidated file contents is a vulnerability where an attacker can upload a malicious file to a web application. This can be done by exploiting the lack of authentication or authorization checks on the server-side of the application. Examples of this attack include uploading a malicious script or executable to a vulnerable web application. These files can then be used to gain access to the application and its data.

# **Examples of Code Requests and Responses**

The following example code shows an insecure file upload request and response:

Request:

Copy

```
POST /upload.php HTTP/1.1
Host: example.com
Content-Type: multipart/form-data; boundary=----WebKitFormBoundary7MA4YWxkTrZu0gW

------WebKitFormBoundary7MA4YWxkTrZu0gW
Content-Disposition: form-data; name="uploaded_file"; filename="example.php"
Content-Type: application/x-php

<?php system($_GET['cmd']);?>
------WebKitFormBoundary7MA4YWxkTrZu0gW--

```

Response:

Copy

```
HTTP/1.1 200 OK
Content-Type: text/html; charset=utf-8

File uploaded successfully!

```

# **Real-Life Examples**

Real-life examples of insecure file uploads can include:

- Malicious files uploaded to a website, such as a PHP shell
- Unsecured files being uploaded to a server
- Unvalidated files being uploaded to a database

# **Mitigating Insecure File Uploads**

Insecure file uploads can be mitigated by following these steps:

1. Perform authentication and authorization checks on the server-side of the application.
2. Restrict the types of files that can be uploaded to the web application.
3. Validate that the uploaded file is of the expected type.
4. Ensure that the uploaded files are stored securely.
5. Perform regular scans of the uploaded files for malicious content.

## Insecure File Uploads Test Example

![image.png](image.png)

![image.png](image%201.png)