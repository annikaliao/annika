---
toc: true
comments: true
layout: post
title: Computers and Networks (Unit 4)
description: Add Definitions from Unit 4 Computer Systems and Networks
categories: []
type: ap
week: 29
---

## Requirements
> Work through College Board Unit 4... blog, add definitions, and pictures.  Be creative, for instance make a story of Computing and Networks that is related to your PBL experiences this year.


### How a Computer Works
> As we have learned, a computer needs aa program to do something smart.  The sequence of a program initiates a series of actions with the computers Central Processing Unit (CPU). This component is essentially a binary machine focussing on program instructions provided.  The CPU retrieives and stores the data it acts upon in Random Access Memory (RAM). Between the CPU, RAM, and Storage Devices a computer can work with many programs and large amounts of data.

List specification of your Computer, or Computers if working as Pair/Trio
- Processor GHz: 1.19 GHz
- Memory in GB: 8 GB
- Storage in GB: 237 GB
- OS: 19045.2728

Define or describe usage of Computer using Computer Programs. Pictures are preferred over a lot of text.  Use your experience.
- **Input devices:** used to provide data or information to a computer. Some common input devices include keyboards, mice, and scanners.
- **Output devices:** used to display or present data or information processed by the computer. Some common output devices include monitors, printers, and speakers.
- **Program File:** a collection of instructions that tell a computer what to do. These instructions are saved in a file format that can be read and executed by the computer. 
- **Program Code:** the set of instructions written in a specific programming language that a computer understands and can execute. It consists of keywords, variables, functions, and other programming constructs.
- **Processes:** a program or set of programs that are currently running on a computer. Each process has its own memory space and resources allocated to it, allowing multiple programs to run simultaneously.
- Ports: A port is a connection point between a computer and an external device or network. Ports can be physical or virtual and allow for data transfer between devices or networks.
- **Data File:** a file that contains information in a specific format that can be read and processed by a computer program. Data files can be created and edited using various software applications.
- Inspect Running Code: Inspecting running code refers to the process of examining the code of a program while it is currently executing. This can be done using debugging tools and allows developers to identify and fix errors in their code.
- **Inspect Variables:** the process of examining the values of variables used in a program. This can be done using debugging tools and allows developers to track how variables change as the program executes.

![](https://i.imgur.com/gdqT6l6.png)

![Computer Hardware]({{site.baseurl}}/images/cpu.jpeg)


### The Internet
> Watch/review College Board Daily Video for 4.1.1

- Essential Knowledge
    - A computing device is a physical artifact that can run a program. Some examples include computers, tablets, servers, routers, and smart sensors.
    - A computing system is a group of computing devices and programs working together for a common purpose.
    - A computer network is a group of interconnected computing devices capable of sending or receiving data.
    - A computer network is a type of computing system. 
    - A path between two computing devices on a computer network (a sender and a receiver) is a sequence of directly connected computing devices that begins at the sender and ends at the receiver.
    - Routing is the process of finding a path from sender to receiver.
    - The bandwidth of a computer network is the maximum amount of data that can be sent in a fixed amount of time.
    - Bandwidth is usually measured in bits per second

- Complete Vocabulary Matching Activity.  Incorporate this into your learnings from year.  To analyze measure path and latency use `traceroute` and `ping` commands from Linux Terminal.  
    - **Path:** a) is a sequence off directly connected computing devices that begins at the sender and ends at the receiver
    - **Route:** e) is the process of finding a path fom sender to receiver 
    - **Computer System:** b) is a group of computing devices and programs working together for a common purpose
    - **Computer Device:** c) is a physical artifact that can run a program. i.e., computers, tablets, servers, routers, and smart sensors
    - **Bandwidth:** d) the maximum amount of data that can be sent in a fixed amount of time
    - **Computer Network:** f) is a group of interconnected computing devices capable of sending or receiving data

> Watch/review College Board Daily Video 4.1.2

- Essential Knowledge
    - The internet is a computer network consisting of interconnected networks that use standardized, open (nonproprierary) communication protocols.
    - Access to the internet depends on the ability to connect a computing device to an internet connected device.
    - A protocol is an agreed-upon set of rules that specify the behavior of a system.
    - The protocols used in the internet are open, which allows users to easily connect additional computing devices to the internet.
    - Routing on the internet is usually dynamic; it is not specified in advance
    - The scalability of a system is the capacity for the system to change in size and scale to meet new demands.
    - The internet was designed to be scalable
    - Information is passed through the internet as a data stream. Data streams contain chunks of data, which are encapsulated in packets. 
    - Packets contain a chunk of data and metadata used for routing the packet between the origin and the destination on the internet, as well as for data reassembly.
    - Packets may arrive at the destination in order, out of order, or not at all
    - IP, TCP and UDP are common protocols used on the internet.
    - The world wide web is a system of linked pages, programs, and files.
    - HTTP is a protocol used by the world wide web
    - The world wide web uses the internet

-  Complete True of False Questions
    - **True**: Open standards and protocols enable different manufacturers and developers to build hardware and software that can communicate with hardware and software on the rest of the internet
    - **False**: IETF is a task force used to enforce laws to keep manufacturers out of the internet
        - IETF (Internet Engineering Task Force) manaes the development of standards and technical discussions concerning the internet in an open and collaborative process
    - **False**: Routes are determined in advance and are not flexible
        - Routes can be dynamically determined and changed based on various factors such as network congestion, routing protocol changes, and link failures. The flexibility of routing is essential for efficient and reliable network communication.
    - **True**: A protocol is an agreed-upon set of rules that specify the behavior of a system
    - **False**: UDP guarantees transfers and is faster
        - UDP (User Datagram Protocol) is a connectionless protocol that does not guarantee the delivery of packets or provide any error-checking mechanisms. While UDP can be faster than other protocols such as TCP, it is not suitable for applications that require reliable data transfer
    - **False**: The World Wide Web is the internet
        - This statement is false because the World Wide Web is just one part of the internet. The internet is a global network of interconnected computer networks, while the World Wide Web is a collection of web pages, websites, and multimedia content that are accessed via the internet.
    - **True**: HTTP is a protocol used by the World Wide Web

- Go over AP videos, vocabulary, and essential knowledge.  Draw a diagram showing the internet and its many levels. A preferred diagram would using your knowledge of frontend, backend, deployment, etc.  Picture would highligh vocabulary by illustration. The below illustration have some ideas

![TCP/IP Process](https://i.imgur.com/vgH0t0F.png)
![DNS Process](https://i.imgur.com/ow7kQl1.png)
![OSI Process](https://www.imperva.com/learn/wp-content/uploads/sites/13/2020/02/OSI-7-layers.jpg)

![Full Stack]({{site.baseurl}}/images/fullstack.png)


- Often we draw pictures of machines communicating over the Internet with arrows.  However, the real communication goes through protocol layers and the machine and then is trasported of the network.   For College Board and future Computer Knowledge you should become familiar with the following ...

```
     User Machine  <---> Frontend Server <---> Backend Server
    +-----------+         +-----------+         +-----------+
    |  Browser  |         |  GH Page  |         |   Flask   |
    +-----------+    ^    +-----------+    ^    +-----------+
    |    HTTP   |    |    |    HTTP   |    |    |    HTTP   |
    +-----------+    |    +-----------+    |    +-----------+
    |    TCP    |    |    |    TCP    |    |    |    TCP    |   
    +-----------+    |    +-----------+    |    +-----------+
    |     IP    |    V    |     IP    |    V    |     IP    |
    +-----------+         +-----------+         +-----------+
    |  Network  |  <--->  |  Network  |  <--->  |  Network  |
    +-----------+         +-----------+         +-----------+
```

The "http" layer is an application layer protocol in the TCP/IP stack, used for ***communication between web browsers and web servers***. It is the protocol used for transmitting data over the World Wide Web.

The "transport" layer (TCP) is responsible for providing reliable data transfer between applications running on different hosts.  The TCP protocol segments the data into smaller ***chunks called "segments"***. Each segment contains a sequence number that identifies its position in the original stream of data, as well as other control information such as source and destination port numbers, and checksums for error detection.

The "ip" layer is responsible for packetizing data received from the TCP layer of the protocol stack, and then ***encapsulating the data into IP packets***. The IP packets are then sent to the lower layers of the protocol stack for transmission over the network.

The "network" layer is responsible for ***routing data packets between networks*** using the Internet Protocol (IP). This layer handles tasks such as packet addressing and routing, fragmentation and reassembly, and ***network congestion*** control.


### Fault Tolerance
> Watch both Daily videos for 4.2

- Essential Knowledge
    - The Internet has been engineered to be fault-tolerant, with abstractions for routing and transmitting data
    - *Redundancy* is the inclusion of extra components that can be used to mitigate failure of a system if other components fail
    - One way to accomplish network redundancy is by having more than one path between any connected devices
    - If a particular device or connection on the Internet fails, subsequent data will be sent via a different route, if possible
    - When a system can support failures and still continue to function, it is called fault-tolerant. This is important because elements of complex systems fail at unexpected times, often in group, and fault tolerance allows users to continue to use the network
    - Redundancy within a system often requires additional resources but can provide the benefit of fault tolerance
    - The redundancy of routing options between two points increases the reliability of the Internet and helps it sclae to the more devices and more people

- Complete the network activity, summarize your understanding of fault tolerance.

|  | ![](https://i.imgur.com/ZOGVfiD.jpg) | ![](https://i.imgur.com/EmIc0UB.jpg) |
| --- | --- | --- |
| Pros | - Uses less resources | - One path goes down, all devices can still communicate (fault-tolerant) <br> - Faster communication |
| Cons | - One path failure causes major problem <br> - Slow communication | - Uses more resources |

In fault tolerance, each device is fault-tolerant, aka still able to communicate with each other even if a path goes down. This is achieved through redundancy, when one device has several paths to and from it. Fault tolerance increases reliability and availability of services. 


### Parallel and Distributed Computing
> Review previous lecture on Parallel Computing and watch Daily vidoe 4.3.  Think of ways to make something in you team project to utilize Cores more effectively.  Here are some thoughts to add to your story of Computers and Networks...

- What is naturally Distributed in Frontend/Backend architecture?  
    - In a frontend/backend architecture, the frontend is naturally distributed because it is responsible for handling user interactions and presenting data to the user, often through a web browser. The backend is also naturally distributed because it handles the processing and storage of data, often across multiple servers or databases.
- Analyze this command in Docker: ```ENV GUNICORN_CMD_ARGS="--workers=1 --bind=0.0.0.0:8086"```.   Determine if there is options are options in this command for parallel computing within the server that runs python/gunicorn.  Here is an [article](https://medium.com/building-the-system/gunicorn-3-means-of-concurrency-efbb547674b7)
    - The command ENV GUNICORN_CMD_ARGS="--workers=1 --bind=0.0.0.0:8086" is used to set an environment variable GUNICORN_CMD_ARGS that configures the Gunicorn web server. The "--workers=1" option specifies the number of worker processes that Gunicorn will spawn to handle incoming requests. In this case, only one worker process will be created. The "--bind=0.0.0.0:8086" option specifies the IP address and port number that Gunicorn will bind to. In this case, Gunicorn will bind to all available network interfaces (0.0.0.0) on port 8086. So, the command sets the configuration options for the number of worker processes and the IP address and port that the Gunicorn server will listen on.

> Last week we discussed parallel computing on local machine.  There are many options.  Here is something to get parallel computing work with a tool called Ray.
- Review this [article](https://www.anyscale.com/blog/writing-your-first-distributed-python-application-with-ray)...  Can you get parallel code on images to work more effectively?  I have not tried Ray.

- Code example from ChatGPT using squares.  This might be more interesting if nums we generated to be a lot bigger.

```python
import ray

# define a simple function that takes a number and returns its square
def square(x):
    return x * x

# initialize Ray
ray.init()

# create a remote function that squares a list of numbers in parallel
@ray.remote
def square_list(nums):
    return [square(num) for num in nums]

# define a list of numbers to square
nums = [1, 2, 3, 4, 5]

# split the list into two parts
split_idx = len(nums) // 2
part1, part2 = nums[:split_idx], nums[split_idx:]

# call the remote function in parallel on the two parts
part1_result = square_list.remote(part1)
part2_result = square_list.remote(part2)

# get the results and combine them
result = ray.get(part1_result) + ray.get(part2_result)

# print the result
print(result)

```
