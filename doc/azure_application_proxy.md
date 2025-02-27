##### Abusing Azure Application Proxy for C2

Attackers can leverage Azure Application Proxy (AAP) to establish a covert C2 channel by tunneling traffic through Microsoft’s cloud infrastructure. AAP provides remote access to internal applications via **\*.msappproxy.net**, which adversaries can exploit to proxy C2 traffic, evade network-based detections, and bypass geo-blocking or IP filtering.

Advantages:
- Avoids direct connections to attacker C2 servers.
- Bypasses firewalls & proxies (whitelisted Microsoft traffic).
- Resilient infrastructure using Microsoft’s cloud.
- Stealthy exfiltration via AAP tunneling.

For more details on AppProxyC2, read the blog: https://www.trustedsec.com/blog/azure-application-proxy-c2

![approxy](doc/appproxyc2.png)