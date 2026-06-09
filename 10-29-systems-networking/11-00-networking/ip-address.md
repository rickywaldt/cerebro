# IP Address

An IP Address is 32 bits in total. The /24 means that 24 bits are reserved for the network and the remaining 8 bits available for the host. Since bits are binary, the formula is 2^(32 - prefix length). In this case, 2^8=256 IP Addresses of which 254 usable. The first and last one are reserved for the network itself and the broadcast, respectively.

Every time you decrease the prefix length by 1, you double the address space. So from /24 to /23 is doubling 256, which is 512 minus 2, so you'll have 510 usable IP Addresses with a /23 subnet.
