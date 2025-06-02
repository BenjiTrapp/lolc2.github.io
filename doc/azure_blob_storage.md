##### Abusing Azure Blob Storage for C2

Attackers can exploit Azure Blob Storage to proxy traffic into internal networks by tunneling data through blob containers. This technique turns Azure’s storage endpoints into a covert channel, enabling reverse SOCKS5-like communication that can bypass egress controls—especially in environments that allow outbound traffic to *.blob.core.windows.net.

proxyblob project:

![proxyblob socks](/doc/proxyblob_socks.png)

![proxyblob demo](/doc/proxyblobgif.gif)