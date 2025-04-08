##### Abusing Google Slides for Command and Control (C2)

Threat actors can exploit Google Slides to establish an infrastructure-less C2 channel by embedding commands within table cells of shared presentations. Compromised systems periodically poll these cells for instructions and update them with execution results using the Google Slides API, effectively blending malicious traffic with legitimate Google services

![google slides](/doc/google_slides.png)