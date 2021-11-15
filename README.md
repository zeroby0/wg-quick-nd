# wg-quick-nd

Like [`wg-quick`](https://man7.org/linux/man-pages/man8/wg-quick.8.html), but doesn't override default route.

The `wg-quick` command from [wireguard-tools](https://github.com/WireGuard/wireguard-tools/blob/master/src/wg-quick/linux.bash) changes the default route of your computer from your router to the VPN server. This makes all the traffic from your computer use the encrypted wireguard connection.

Usually this is desired, but I want only some of my programs to connect to the server, and everything else to connect directly to the Internet.

wg-quick-nd is a drop-in replacement to wg-quick that doesn't override your default route. Programs that need VPN access will be placed in a linux network namespace that is connected to wiregaurd.

## License

All the code here is modified from https://github.com/WireGuard/wireguard-tools/blob/master/src/wg-quick/linux.bash.

The original program is licensed as GNU GPL V2, and so this program is too.
