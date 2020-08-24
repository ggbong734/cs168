_Self study notes taken from lecture slides_

# CS 168: Introduction to the Internet: Architecture and Protocols
*(Spring 2020 coursework)*
*Instructor: Sylvia Ratnasamy, Murphy McCauley*

1. Internet
2. Protocols
3. Architecture

## Internet

### L2: How the Internet Works

The Internet transfers data between endhosts:

<p align="center"><img src="images/internet_data.png" height= "150"/></p>

Communication between a pair of endpoints involve sending **packets** of data:
- Packets are chunk of bits with headers
- Header contains destination address and name

Packets are transmitted from endhosts via **links**:
- Bandwidth: Number of bits transmitted per unit time
- Propagation delay: time it takes to travel along the link

Time taken to send packets: Transmission delay, propagation delay, queue delay.

Network resources are shared between end hosts. They are **statistically multiplexed**.
- Demands are combined to share resources efficiently anad hope that peak rates don't occur at same time
- Based on the premise that peak of aggregate load is << aggregate of peak loads

---
### L3: Architectural Principles

Two approaches to sharing network resources:
1. Reservations/**circuit switching**: End-hosts reserve bandwidth when needed
2. On demand/**packet switching**: Data packets are sent as they emerge. Resources given out on packet by packet basis.

Pros for circuit switching:
- More predictable performance (reserved bandwidth)
- No queues
- Used by telephone network

Pros for packet switching:
- Better efficiency
- Faster startup
- Easier recover from failure
- Simpler implementation 
- Used by Internet
 
#### Network System Modularity

Protocol
> agreement between parties on **how to communicate**. Deines the syntax of communication. Exists at hardware and software level.

<p align="center"><img src="images/network_layers.png" height= "150"/></p>

Notice there is only one IP layer! 

Lower three layers implemented everywhere. Top two layers implemented only at hosts. 

<p align="center"><img src="images/end_system.png" height= "150"/></p>

Operating System (OS) supports **logical ports**:
- place where app connects to OS network stack

Socket 
> an OS mechanism that connects app processes to the network stack

When an app wants to access to the network, it opens a socket which is associated with a port. 

The port number is use by the OS to direct incoming packets to its associated socket.

<p align="center"><img src="images/logical_ports.png" height= "150"/></p>

## Protocols










## Architecture



