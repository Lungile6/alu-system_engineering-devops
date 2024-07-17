
---

# Web Server Project

## General Overview

This project involves the development and understanding of a web server, focusing on its core functionalities, process management, and DNS configurations. Below are the detailed explanations and requirements for this project.

## What is the Main Role of a Web Server?

A web server's main role is to store, process, and deliver web content to clients over the internet. It handles incoming requests from clients (such as web browsers) and serves the requested resources or data.

### Key Functions of a Web Server:
1. **Serving Static Content**: Providing files such as HTML, CSS, JavaScript, and images to clients.
2. **Dynamic Content Handling**: Executing server-side scripts to generate dynamic web pages.
3. **Resource Management**: Efficiently managing hardware resources and network connections.
4. **Security**: Implementing security protocols (e.g., HTTPS, SSL/TLS) to secure data transmission.
5. **Load Balancing**: Distributing incoming traffic across multiple servers to ensure reliability and performance.

## What is a Child Process?

A child process is a subprocess created by a parent process. In web servers, child processes are often used to handle individual client requests concurrently.

### Characteristics:
- **Independent Execution**: Runs concurrently with the parent process.
- **Resource Sharing**: Inherits open files and environmental variables from the parent.
- **Separate Memory Space**: Operates in a separate memory space, ensuring stability and security.

## Why Web Servers Usually Have a Parent Process and Child Processes

Web servers use a parent-child process architecture to manage multiple client requests efficiently.

### Advantages:
1. **Concurrency**: Multiple child processes can handle numerous client requests simultaneously, improving server responsiveness.
2. **Stability**: If a child process fails, the parent process can create a new one, ensuring continuous service.
3. **Security**: Child processes can run with restricted privileges, limiting the potential damage from security breaches.
4. **Scalability**: The server can dynamically adjust the number of child processes based on the current load.

## What are the Main HTTP Requests?

HTTP (Hypertext Transfer Protocol) defines several types of requests that clients can make to servers. The main HTTP requests include:

1. **GET**: Requests data from a specified resource. Should only retrieve data and not have any other effect.
2. **POST**: Submits data to be processed to a specified resource. Often used when submitting form data.
3. **PUT**: Uploads a representation of the specified resource. Used to update existing resources or create a new resource if it doesn't exist.
4. **DELETE**: Removes the specified resource.
5. **HEAD**: Similar to GET but without the response body. Used to retrieve the headers of a resource.
6. **OPTIONS**: Describes the communication options for the target resource.
7. **PATCH**: Applies partial modifications to a resource.

## DNS

### What Does DNS Stand For?

DNS stands for Domain Name System.

### What is DNS Main Role?

The main role of DNS is to translate human-readable domain names (like www.example.com) into IP addresses (like 192.168.1.1), which computers use to identify each other on the network. This process is known as domain name resolution.

### DNS Record Types

DNS records are used to map domain names to various types of data, such as IP addresses or other domain names. The main DNS record types include:

1. **A Record (Address Record)**:
   - Maps a domain name to a corresponding IPv4 address.
   - Example: `example.com. IN A 192.0.2.1`

2. **CNAME Record (Canonical Name Record)**:
   - Maps a domain name to another domain name (aliasing).
   - Useful for pointing multiple domain names to the same IP address.
   - Example: `www.example.com. IN CNAME example.com.`

3. **TXT Record (Text Record)**:
   - Stores text information. Often used for domain verification and to provide additional information to email servers (like SPF, DKIM, and DMARC).
   - Example: `example.com. IN TXT "v=spf1 include:_spf.example.com ~all"`

4. **MX Record (Mail Exchange Record)**:
   - Specifies the mail servers responsible for receiving email on behalf of a domain.
   - Example: `example.com. IN MX 10 mail.example.com.`

## Conclusion

This README.md file provides a comprehensive overview of the web server project, covering its main functions, process management, HTTP requests, and DNS configurations. This foundational knowledge is crucial for developing and understanding web server operations and their integration into network infrastructures.

---