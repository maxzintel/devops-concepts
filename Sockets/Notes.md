# Sockets
#### Allow 2 different processes to communicate with each other from same/different machines.
* A way to talk to other computers via Unix file descriptors.
* Used in client/server app frameworks.
  * Network protocols like FTP, SMTP, and POP3 use it to establish connections between the client and server.
* Most Commonly Used Socket Types:
  * **Stream Sockets** - Delivery guaranteed in a networked environment.
    * Use TCP (Transmission Control Protocol)
    * If you send "A" "B" "C" in that order, the data will be received in that order.
  * **Datagram Sockets** - Delivery NOT guaranteed in a networked environment.
    * "Connectionless" => You don't need to have an open connection like is needed in Stream Sockets.
    * Must build a packet and send it out via destination info included in the packet.
    * Uses UDP (User Datagram Protocol).
