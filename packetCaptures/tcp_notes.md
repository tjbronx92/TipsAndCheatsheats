# TCP Protocol Notes

## TCP Flags

**SYN (synchronization)**
> First step of 3-way handshake, the initial packet that allows the client to set the first sequence number for request packets originating from the client. 

**SYN/ACK (synchronization / acknoewldgement)**
> Second step of 3-way handshake, response to the SYN packet with an SYN/ACK packet. This packet confirms the sequence number sent by the client by acknowledging it.

**ACK (acknoewldgement)**
> Final step of 3-way handshack, the client responds to the SYN/ACK packet with an ACK packet that acknowledges the server’s sequence number request.

**PSH (push)**
> Flag instructs the receiving device to deliver the data immediately to the application layer without waiting for more data to arrive.

**RST (reset)**  
Reasons why a packet has the RST flag set:
1. > The packet is an initial SYN packet trying to establish a connection to a server port on which no process is listening. 

2. > The packet arrives on a TCP connection that was previously established, but the local application already closed its socket or exited and the OS closed the socket.

---
Reference:

<sup>1</sup> [Understanding TCP PSH Packet Flag
](https://orhanergun.net/understanding-tcp-psh-packet-flag)

<sup>2</sup> [SYN/ACK in the TCP Protocol](https://www.baeldung.com/cs/tcp-protocol-syn-ack)

<sup>3</sup> [What is a TCP Reset (RST)?](https://www.pico.net/kb/what-is-a-tcp-reset-rst/)

<sup>4</sup> [TCP Flags: PSH and URG](https://packetlife.net/blog/2011/mar/2/tcp-flags-psh-and-urg/)