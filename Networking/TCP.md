# TCP

A packet in TCP is called `Segment`

Transport Layer is responsible for process to process delivery of the message. 



TCP stands for Transmission Control Protocol which is a reliable transport layer or layer 4 protocol. Since it is present between the Application Layer and Network layer, it also acts as an intermediary between application programs and network operations.

TCP provides process to process communication using port numbers. Some well known port numbers that are used by TCP are:
- Port 7 for `Echo` - echoes a received datagram back to the sender.
- Port 9 for `Discard` - Discards any datagram that is received.
- Port 11 for `Users` - Active users
- Port 13 for `Daytime` - Returns the date and time
- Port 17 for `Quote` - Returns a quote of the day
- Port 19 for `Chargen` - Returns a string of characters
- Port 20 and 21 for `FTP` - File Transfer Protocol (Data and Control)
- Port 23 for `Telnet` - Terminal Network
- Port 25 for `SMTP` - Simple Mail Transfer Protocol
- Port 53 for `DNS` - Domain Name Server
- Port 67 for `BOOTP` - Bootstrap Protocol
- Port 79 for `Finger` - Finger
- Port 80 for `HTTP` - HTTP

TCP is a stream-oriented protocol which means TCP allows the sending process to deliver data as a stream of bytes and allows the receiving process
to obtain data as a stream of bytes.


`Sending and Receiving Buffers`

TCP uses the concept of sending and receiving buffers (one for each direction) for sending and receiving streaming data. One way to implement a buffer is to setup a circular array. The circular array is broken down into 3 chambers. One chamber or section that is empty which is going to contain the data to be sent by the sending process (producer), the second chamber contains the data that has been sent but not ack'd yet. Once it is ack'd it will be purged. The third section contains the data that is going to be sent by the sending TCP. 

The receiving buffer is rather simpler than the sending one as it just contains 2 sections/chambers. One is the empty set of bytes that can be filled once the data will be received. The second is the chamber that has the received bytes, yet to be consumed by the receiving process. Once it will be consumed, they will be purged allocating more room for newer data.



`Full Duplex Communication` - TCP offers full duplex communication that means the data can be sent and received at the same time. Each TCP has the sending and receiving buffers, and segments can move in any direction.

`Multiplexing and Demultiplexing` - 



