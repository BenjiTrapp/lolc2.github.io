##### Abusing Microsoft Graph API for C2

Adversaries can exploit the Microsoft Graph API **`https://graph.microsoft.com`** to establish covert command-and-control (C2) channels by leveraging legitimate Microsoft 365 services such as OneDrive, SharePoint, Outlook, Teams, and Excel Online. By embedding malicious communications within these cloud applications, attackers evade traditional security controls and persist within an enterprise environment.

Reconnaissance activities include querying Azure AD to enumerate users, roles, and permissions before escalating access (**`/me`**).

OneDrive and SharePoint serve as staging grounds for payloads, allowing adversaries to fetch commands and exfiltrate data by reading and writing tasking files in shared folders (**`/me/drive/root/children`**, **`/sites/*/drives`**).

Outlook can be abused to hide commands inside draft emails (**`/me/MailFolders/drafts/messages`**) and exfiltrate data through regular messages (**`/me/messages`**).

Microsoft Teams enables adversaries to send commands disguised as normal chat messages, using channels and direct messages (**`/beta/*metadata#chats`, `/beta/*metadata#teams*/channels*/messages`**).

Excel Online can function as a covert exfiltration method, where adversaries modify hidden worksheets to store stolen data (**`/drives/*/items/*/workbook/worksheets`**).

Authentication abuse plays a critical role in persistence, with attackers leveraging OAuth tokens to maintain long-term Graph API access (**`/oauth2/v2.0/token`**).


SharePoint Lists can be manipulated to store encoded commands, ensuring a stealthy communication method between attackers and compromised endpoints (**`/sites/*/lists/*`**).

By abusing these Graph API endpoints, adversaries blend malicious C2 traffic with normal enterprise activity, making detection significantly more challenging.

A must-read for anyone interested in Microsoft Graph API abuse for C2: https://redsiege.com/blog/2024/01/graphstrike-developer/

![graphstrike](/doc/graphstrike.png)
