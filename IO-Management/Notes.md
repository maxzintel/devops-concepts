# Software I/O at OS level:
#### Kernel I/O Subsystem performs the following tasks:
1. Scheduling - Sets queue for requests. Rearranges queue where needed.
2. Buffering - There is a memory area maintained called the `buffer`. It stores data while the data is transferred between devices/operations. Its main use is to cope with the difference in speed between the producer and the consumer.
3. Caching - Memory cahce that holds copies of data.
4. Spooling and Device Restoration - A buffer that holds output for a device. Found in `/var` in Linux. Main example is the connection between a computer and a printer. Copies queued are spooled one at a time.
5. Error Handling - possible on systems with `protected memory`.
