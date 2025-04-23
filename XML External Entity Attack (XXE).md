# XML External Entity Attack (XXE)

[](https://rkive.gitbook.io/~gitbook/image?url=https%3A%2F%2F3577347090-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FWrIcinZ87qSasUAtuqcU%252Fuploads%252FN1zPdMSM4NGxjQZ7fIWd%252Fimage.png%3Falt%3Dmedia%26token%3D2aafb75a-bd23-4c55-965d-45dcdacfdd3f&width=768&dpr=4&quality=100&sign=b9bd6ca1&sv=2)

# XML External Entity (XXE)

> XML External Entity (XXE) attack is a type of attack that exploits a vulnerability in an XML parser that is used to process XML documents. This vulnerability can be used by attackers to gain access to sensitive data within an XML file, or even to gain access to a network system.
> 

# **What is an XML External Entity Attack?**

An XML External Entity (XXE) attack occurs when an XML document is parsed with an XML parser that is vulnerable to XXE. This vulnerability can be exploited by an attacker to read data from the XML document, or even to gain access to the network. It is important to note that an XXE attack does not require the attacker to have any knowledge of the XML document or the XML parser.

XML External Entity attacks are also known as “XML Injection” or “XML Bombing”. XXE attacks occur when an XML document is parsed with an insecure XML parser, which can be used by an attacker to gain access to sensitive data within the XML document or to gain access to a network system.

# **How Does an XML External Entity Attack Work?**

An XXE attack is a type of attack that exploits a vulnerability in an XML parser that is used to process XML documents. XML parsers are commonly used to process data from a web service or application. The vulnerability is caused by the fact that the XML parser has not been configured to properly validate the XML document before processing it.

When an attacker attempts to exploit this vulnerability, they will send a specially crafted XML document to the vulnerable XML parser. The document will contain a malicious code that will allow the attacker to gain access to the sensitive data within the XML document, or to gain access to a network system.

The malicious code can be written in a variety of languages and can be used to steal data from the XML document or to gain access to the network. It is important to note that the malicious code does not have to be written in the same language as the XML parser, as the XML parser will not be able to detect the malicious code.

# **Examples of XML External Entity Attacks**

There are many different types of XXE attacks, and each type of attack can be used to gain access to sensitive data or to gain access to a network system. Here are some examples of XXE attacks that can be used to exploit a vulnerable XML parser:

- XML Injection: This type of attack occurs when an attacker sends a specially crafted XML document to the vulnerable XML parser. The document contains malicious code which can be used to steal data from the XML document or to gain access to the network system.
- XML Bombing: This type of attack occurs when an attacker sends a specially crafted XML document to the vulnerable XML parser. The document contains malicious code which can be used to cause a denial of service (DoS) attack or to gain access to the network system.
- XXE Injection: This type of attack occurs when an attacker sends a specially crafted XML document to the vulnerable XML parser. The document contains malicious code which can be used to gain access to the network system or to execute arbitrary code on the system.

It is important to note that an XXE attack can be used to exploit a vulnerable XML parser in order to gain access to sensitive data or to gain access to a network system. As such, it is important for organizations to ensure that their XML parsers are properly configured and secure.

# **Prevention**

1. Ensure all external resources are validated and filtered to avoid malicious entities from being parsed.
2. Use the latest version of XML parsers which are equipped to handle external entities safely.
3. Always set the entity resolver to an empty object when parsing untrusted XML documents.
4. Disable external entity parsing when possible.
5. Use whitelisting when validating XML documents to ensure only known, safe elements are being processed.
6. Check for the presence of a DTD in the XML document, as they can be used to enable XXE attacks.
7. Use a Content Security Policy (CSP) to prevent attackers from exploiting XXE vulnerabilities.
8. Use input validation to detect and prevent malicious entities from being parsed.

[XSS Attack Example](https://www.notion.so/XSS-Attack-Example-1a377dd38d678012944ac10babf2db18?pvs=21)