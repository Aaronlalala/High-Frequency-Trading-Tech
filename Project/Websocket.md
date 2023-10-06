# I/O-Bound

I/O-bound operations are tasks that spend most of their time waiting for external resources to respond, rather than using the CPU to compute. There external resources can be disk drives, network interface, databases or use input. They are often good to use asynchronous programming.



# WebSocket

WebSocket is a communication protocol that provides two-directional, low latency, real-time and persistent communication channels over a TCP connection. 

HTTP protocol requires client to initiate requests to the server to give responses.



# Why WebSocket is I/O-Bound

WebSockets involve network communication between a client and a server. When you send or receive data over a WebSocket, the program has to wait for the network to transmit the data. This waiting is typically I/O-bound.