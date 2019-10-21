# pingety-ping

Colorized terminal-mode bar-charting for ping

## Why

Mainly this came out of frustration with in-flight wifi, which is never great and often completely absent. I like to have a terminal window open pinging a well-known IP address so I instantly see the status of my network connection -- not the flawless four-bar signal to the onboard router, but the status *from there onward*.

Since ping times vary by several orders of magnitude -- less than 10 ms for good land fiber, 100 ms or so for VPN, 1000-2000 ms for in-flight -- a logarithmic scale is necessary.

## How

You can supply a ping target, e.g. `pingety-ping 8.8.8.8`, to use a script-internal (ruby-lib) pinger.

Or, you can use `-i` to pipe in the output of the system `ping` command, e.g. `ping 8.8.8.8 | pingety-ping -i`.

## Screenshots


