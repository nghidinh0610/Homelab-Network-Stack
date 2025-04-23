# Homelab-Network-Stack
A self-hosted home network utilizing old laptop as a mini server. Designed to enable secure remote access, DNS filtering, web traffic control and file sharing. The goal of this project is minimal cost and maximum performance

<h2>Stack Overview</h2>

<table>
  <tr>
    <th>Service</th>
    <th>Role</th>
  </tr>
  <tr>
    <td> Ubuntu</td>
    <td>Base OS on repurposed laptop</td>
  </tr>
  <tr>
    <td> WireGuard</td>
    <td>Encrypted VPN access to local network</td>
  </tr>
  <tr>
    <td> Pi-hole</td>
    <td>DNS-based ad/tracker blocking for all clients</td>
  </tr>
  <tr>
    <td> Squid</td>
    <td>HTTP/S proxy for filtering, caching, and logging</td>
  </tr>
  <tr>
    <td> DuckDNS</td>
    <td>Dynamic DNS for remote VPN access</td>
  </tr>
  <tr>
    <td> Samba</td>
    <td>Local file sharing across devices (PCs, phones)</td>
  </tr>
</table>

<h2>Network Flow</h2>

<pre>
[ Remote Device ]
     ↓  (Encrypted via WireGuard)
[ Laptop Server ]
     ↓  (Squid Proxy filters HTTP/S)
[ Pi-hole DNS Filtering ]
     ↓
[ Internet ]
</pre>

<h2>What I Did</h2>
<ul>
  <li> Converted unused laptop into a self-hosted multi-service server</li>
  <li> Set up WireGuard VPN with DuckDNS for secure remote access</li>
  <li> Deployed Pi-hole to block trackers and ads </li>
  <li> Configured Squid proxy for web traffic logging, filtering, and caching</li>
  <li> Enabled Samba shares for LAN file access between multiple devices</li>
  <li> Monitored DNS & proxy logs for transparency and traffic auditing</li>
  <li> Automated DuckDNS updates using <code>cron</code> and shell scripting</li>
</ul>

<h2>Results</h2>
<ul>
  <li>90% ad/tracker reduction across all connected devices</li>
  <li>Faster repeated web browsing via proxy caching</li>
  <li>100% secure remote access to home network from any device</li>
  <li>Full control and visibility of network traffic</li>
</ul>

<h2>Tools & Tech</h2>
<p><code>Ubuntu Server</code> | <code>WireGuard</code> | <code>Pi-hole</code> | <code>Squid</code> | <code>DuckDNS</code> | <code>Samba</code><br>
<code>Bash</code>, <code>iptables</code>, <code>systemd</code>, <code>crontab</code>, <code>ufw</code>, <code>SSH</code></p>
