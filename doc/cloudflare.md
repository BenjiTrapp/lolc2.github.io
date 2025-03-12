##### Abusing Microsoft Cloudflare for C2

Attackers are exploiting Cloudflare Workers, Cloudflare Tunnels, and Cloudflare Apps to establish resilient Command-and-Control (C2) infrastructures. By routing malicious traffic through Cloudflare’s network, they can blend in with legitimate traffic, making detection more difficult. Rather than directly exposing their C2 servers, they leverage Cloudflare as a proxy, complicating efforts to track and block their infrastructure. This technique enables attackers to host payloads, relay commands, and exfiltrate data while benefiting from Cloudflare’s security and reliability.

APT41 has been observed using Cloudflare Workers to deploy serverless code accessible via the Cloudflare CDN, effectively proxying C2 traffic to their own infrastructure.