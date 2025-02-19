##### Abusing DuckDuckGo for C2

Adversaries can exploit DuckDuckGo's image proxy to establish covert command-and-control (C2) channels. By embedding commands within image requests, they can disguise malicious traffic as legitimate search queries. This technique leverages the proxy's lack of domain allow-listing and URI sanitization, enabling the relay of arbitrary data to compromised servers. A proof of concept, DuckDuckC2, demonstrates this method.

![duckduckgo](/doc/duckduckc2.png)