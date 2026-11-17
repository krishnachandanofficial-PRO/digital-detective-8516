# Mission 7 - How computers communicate

## 1. Task / objective

Explain basic network ideas, check a public website and its DNS result, then describe how a website opens in a browser.

## 2. Work completed

### Network concepts

| Concept | What I understand | Example |
| --- | --- | --- |
| LAN | A network in a small area. | Computers connected in one classroom or home. |
| MAN | A network across a city or a large campus. | A network joining buildings around a city. |
| WAN | A network across a much larger area. | The Internet connects networks in different places. |
| DNS | Finds an IP address for a domain name. | `example.com` was looked up before contacting it. |
| Router | Sends data between networks. | A router forwards traffic from a local network to the Internet. |
| Protocol | Rules that computers follow when they communicate. | HTTPS is used for a secure web request. |
| Packet switching | Data is split into smaller packets that can travel over a network. | A website response travels in packets. |
| Client-server | One side asks for a service and the other provides it. | A browser is the client and the website host is the server. |

### Network observations

| Check | Privacy-safe result | What it shows |
| --- | --- | --- |
| `ping -c 3 example.com` | 3 packets sent, 3 received, 0% packet loss | This public domain answered the connectivity test at that moment. |
| `nslookup example.com` | Public addresses `104.20.23.154` and `172.66.147.243` | DNS gave network addresses for the domain. The answer can change later. |
| `curl -I https://example.com` | HTTP/2 status `200` | The website responded to an HTTPS header request. |

A connectivity test helps me check whether my computer can reach a destination and receive a reply. A DNS lookup shows which address a domain name leads to. When I type a website name, DNS lets the browser find an address it can contact.

### Opening a website

1. I type the website link in the browser. The browser is the **client** asking for the page.
2. The browser uses **DNS** to look up the site's IP address, so it knows where to send the request.
3. The request goes through my router and the network using **protocols** such as HTTPS and TCP/IP.
4. The request travels in smaller **packets** to reach the web **server**.
5. The server gets the requested page files and sends a response back in packets.
6. The browser receives the response, loads the page contents and shows the website on the screen.

## 3. Commands / tools used

| Command | Purpose |
| --- | --- |
| `ping -c 3 example.com` | Send three test packets to a public example domain. |
| `nslookup example.com` | Look up the domain's public network addresses. |
| `curl -I https://example.com` | Check the website's HTTPS response headers. |
| `git add`, `git commit`, `git push` | Stage, save and publish this mission. |

## 4. My understanding

When I type a link, DNS looks up the IP address to find the site. The router passes the request through the network to the server, and the server sends the page files back. The browser is the client, and it uses the response to display the page. Protocols give the rules for that communication, and packets let the data travel in smaller pieces.

## 5. Difficulties faced

No major difficulty.

## 6. How I resolved them

Not applicable.

## 7. Evidence / files

This README contains the concept table, safe command results and website explanation. I did not include my own IP address or Wi-Fi details.

## 8. Commit details

Commit message: `Explain networking concepts and website communication`. Pushed to GitHub on the `main` branch.
