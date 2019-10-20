# pingety-ping

Colorized terminal-mode bar-charting for ping

## Why

Mainly this came out of frustration with in-flight wifi, which is never great and often completely absent. I like to have a terminal window open pinging a well-known IP address so I instantly see the status of my network connection -- not the flawless four-bar signal to the onboard router, but the status *from there onward*. If I can see what's going on, I'm less likely to be frustrated by it and more likely to accept the transient phenomena.

Since ping times vary by several orders of magnitude -- less than 10 ms for good land fiber, 100 ms or so for VPN, 1000-2000 ms for in-flight -- a logarithmic scale is necessary.

## Using

You can supply a ping target, e.g. `pingety-ping 8.8.8.8`, to use a script-internal (ruby-lib) pinger.

Or, you can use `-x` to pipe in the output of the system `ping` command, e.g. `ping 8.8.8.8 | pingety-ping -x`.

## Dependencies

```
sudo gem install net-ping
```

## Screenshots

In-flight, high-latency but reliable:

![in-flight.png](https://github.com/johnkerl/pingety-ping/blob/master/screenshots/in-flight.png)

Pinging the onboard router on the same flight -- stellar -- which is why the desktop icon gives a hearty four-bars review to the signal quality, when the reality is more complex:

![onboard-router.png](https://github.com/johnkerl/pingety-ping/blob/master/screenshots/onboard-router.png)

High-variance on local network:

![meh.png](https://github.com/johnkerl/pingety-ping/blob/master/screenshots/meh.png)

Low-quality connection:

![not-great.png](https://github.com/johnkerl/pingety-ping/blob/master/screenshots/not-great.png)

On good fiber -- before, during, and after disconnect from VPN:

![vpn-disconnect.png](https://github.com/johnkerl/pingety-ping/blob/master/screenshots/vpn-disconnect.png)
