# 0x09. Web infrastructure design

## 0. Simple web stack

 The web infrastructure design in [0. Simple web stack](0. Simple web stack) illustrates a one server web infrastructure that hosts the website that is reachable via `www.foobar.com`.

### Server

A server is an actual physical computer. This could also be a virtual machine or container in the cloud era. Hence, a server can be physical or virtual. A server can be thought of as a computer with no keyboard, mouse or screen that can be accessed over a network and runs an operating system (OS).

### The domain name

The domain name is used by the Domain Name System (DNS) resolver to get a request to its intended destination. The domain name is used to look-up an Internet Protocol (IP) address.

### DNS record

`CNAME` is a DNS record that points a subdomain to another domain.
The `www.foobar.com` points to `foobar.com` using `CNAME` while `foobar.com` points to an actual IP address using an `A` record.

### The web server

A web server, often identified as HTTP server, is a software that understands URLs and HTTP.
Its role is to store and deliver static content (html, css files, images, etc.) to an end user's device.

### The application server

An application server serves business logic to application programs through any number of protocols.
Basically, its role is to handle dynamic web content requests.

### The database

The database organizes the collection of information making it easy to access, manage and update.

### HTTP

The server communicates with the user's computer via HTTP/S, a protocol that is part of the TCP/IP suite. This communication happens on port 80 of both computers.

## Drawbacks of this infrastructure

### Single point of failure (SPOF)

A SPOF is a part of a system that, if it fails stops the entire system from working.
In the design the single server is a SPOF.

### Maintenance

Again whenever maintenance is needed, the whole system has to be shut down, leading to planned downtime.

### Increased traffic

As the application of this design grows and number of users increase, the application will have to be scaled horizontally in order to handle increased incoming traffic.
