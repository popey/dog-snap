## dog (ARCHIVED)

> **Note:** The [upstream project](https://github.com/ogham/dog) is abandoned (last release 2021) and is incompatible with modern system libraries. This snap has been unlisted from the Snap Store and this repo is archived.

dog is a command-line DNS client, like `dig`. It has colourful output, understands normal command-line argument syntax, supports the DNS-over-TLS and DNS-over-HTTPS protocols, and can emit JSON.

```text
$ dog --help
dog ● command-line DNS client

Usage:
  dog [OPTIONS] [--] <arguments>

Examples:
  dog example.net                          Query a domain using default settings
  dog example.net MX                       ...looking up MX records instead
  dog example.net MX @1.1.1.1              ...using a specific nameserver instead
  dog example.net MX @1.1.1.1 -T           ...using TCP rather than UDP
  dog -q example.net -t MX -n 1.1.1.1 -T   As above, but using explicit arguments

Query options:
  <arguments>              Human-readable host names, nameservers, types, or classes
  -q, --query=HOST         Host name or IP address to query
  -t, --type=TYPE          Type of the DNS record being queried (A, MX, NS...)
  -n, --nameserver=ADDR    Address of the nameserver to send packets to
  --class=CLASS            Network class of the DNS record being queried (IN, CH, HS)

Sending options:
  --edns=SETTING           Whether to OPT in to EDNS (disable, hide, show)
  --txid=NUMBER            Set the transaction ID to a specific value
  -Z=TWEAKS                Set uncommon protocol-level tweaks

Protocol options:
  -U, --udp                Use the DNS protocol over UDP
  -T, --tcp                Use the DNS protocol over TCP
  -S, --tls                Use the DNS-over-TLS protocol
  -H, --https              Use the DNS-over-HTTPS protocol

Output options:
  -1, --short              Short mode: display nothing but the first result
  -J, --json               Display the output as JSON
  --color, --colour=WHEN   When to colourise the output (always, automatic, never)
  --seconds                Do not format durations, display them as seconds
  --time                   Print how long the response took to arrive

Meta options:
  -?, --help               Print list of command-line options
  -v, --version            Print version information

```
This is an unofficial snap of dog, built from the upstream source at https://github.com/ogham/dog
