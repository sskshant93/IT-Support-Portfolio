## Step 1 - Check Network Configuration

The first step is to review the computer's current network configuration.

```cmd
ipconfig /all
```

### What `ipconfig /all` Tells You

Think of this command as asking the computer: **"What network settings are you currently using?"**

It provides information such as:

- IPv4 address
- Subnet mask
- Default gateway
- DHCP status and server
- DNS servers
- Network adapter information

For example:

```text
IPv4 Address:       192.168.1.25
Subnet Mask:        255.255.255.0
Default Gateway:    192.168.1.1
DHCP Enabled:       Yes
DNS Servers:        192.168.1.1
```

### Troubleshooting Example

If the computer receives an IPv4 address beginning with `169.254`, it may indicate that Windows was unable to obtain an IPv4 address from a DHCP server and assigned itself an APIPA address.


## Step 2 - Test Network Connectivity

After checking the IP configuration, use `ping` to test connectivity at different points in the network.

### Test the Local TCP/IP Stack

```cmd
ping 127.0.0.1
```

Tests the local TCP/IP stack on the computer.

### Test the Default Gateway

```cmd
ping 192.168.1.1
```

Tests whether the computer can communicate with the local router or default gateway.

### Test Internet Connectivity

```cmd
ping 8.8.8.8
```

Tests connectivity to an external IP address without relying on DNS name resolution.

### Test Using a Hostname

```cmd
ping google.com
```

Tests connectivity using a hostname. If an external IP address responds but the hostname does not resolve, DNS may need further investigation.

### What the Results Tell You

- Successful gateway ping → Local network connectivity is working.
- Successful external IP ping → Internet IP connectivity is available.
- External IP works but hostname fails → Possible DNS problem.
- Gateway cannot be reached → Investigate the local network connection, IP configuration, Wi-Fi/Ethernet, or router.

- ## Step 3 - Test DNS Name Resolution

If IP connectivity is working but websites cannot be reached by name, check DNS name resolution.

```cmd
nslookup google.com
```

`nslookup` queries a DNS server to determine whether a hostname can be translated into an IP address.

### What to Check

A successful lookup should return information such as:

```text
Name:       google.com
Addresses:  <resolved IP address>
```

### Troubleshooting Example

If:

- `ping 8.8.8.8` works
- `nslookup google.com` fails

the computer may have internet connectivity, but there may be a DNS configuration or DNS server problem.

The DNS server configured on the computer can be reviewed using:

```cmd
ipconfig /all
```

This helps determine whether the correct DNS server is configured.

## Step 4 - Trace the Network Path

If connectivity problems continue, use `tracert` to examine the path traffic takes toward a destination.

```cmd
tracert google.com
```

`tracert` displays the network hops between the computer and the destination.

### What It Can Help Identify

- Whether traffic is leaving the local network
- Where delays may be occurring
- Where communication may stop along the route
- Whether the issue appears to be local or farther along the network path

A timeout at an individual hop does not always indicate a failure because some routers may not respond to traceroute requests.

## Troubleshooting Summary

| Test | Purpose | Possible Finding |
|---|---|---|
| `ipconfig /all` | Check IP configuration | Incorrect IP, gateway, DHCP, or DNS configuration |
| `ping 127.0.0.1` | Test local TCP/IP stack | Local TCP/IP issue |
| `ping <gateway>` | Test local network connectivity | Local network or gateway issue |
| `ping 8.8.8.8` | Test external IP connectivity | Internet/routing issue |
| `nslookup google.com` | Test DNS resolution | DNS configuration or DNS server issue |
| `tracert google.com` | Examine network path | Helps locate where connectivity may be interrupted |

## Skills Demonstrated

- Windows network troubleshooting
- TCP/IP fundamentals
- IP configuration
- DHCP and APIPA identification
- DNS troubleshooting
- Command Prompt
- Connectivity testing
- Structured troubleshooting methodology
- Technical documentation
