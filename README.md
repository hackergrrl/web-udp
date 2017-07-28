# Web UDP
> Experiment for a web standard for creating and using UDP sockets in the browser.

*(More coming soon!)*

## What?

- a low level browser api granting access to UDP sockets for the purpose of peer-to-peer communications with low overhead

## Why?

WebRTC is very heavy on resources: most modern machines cannot open more than a
dozen connections without slowing their entire system to a crawl. Contrast this
to plain UDP sockets, which a modern machine can easily have many many thousands
of at once at very little resource cost.

WebRTC is a very heavy specification. This means a complex implementation, which
only makes the creation of an implementation available to companies/interests
with a great deal of resources. A simpler implementation allows other vendors
and implementations for other languages to come into the table.

These result in webrtc being ineffective for many interesting and exciting
applications like peer-to-peer apps and real-time games.

Having a simple low level layer, folks can layer non-browser-specific modules on
top. It also means less heavy dependency on browser vendors for support, dev,
features, etc. The community can develop out what it wants. This is *so*
powerful.

(NOTE: mention DHTs: https://github.com/feross/webtorrent/issues/288)

## How?

- xor /w random nonce to scramble payload, to prevent web-udp sites from being
  attacking non-web-udp services /wo explicitly supporting web-udp

## Implementation Vectors

No implementation exists yet, but there are a few different options:

- Local server that acts as a UDP proxy to the browser
- Chrome App: these provide [a UDP API](https://developer.chrome.com/apps/sockets_udp)
  - Google has [decided to nix Chrome Apps](https://blog.chromium.org/2016/08/from-chrome-apps-to-web.html)
- [Beaker Browser](https://github.com/beakerbrowser/beaker): integrate natively
- Fork Chromium and write an implementation

## Other Efforts

https://github.com/Maksims/web-udp-public/ is looking very promising, but it is intended as a web standard for server-client UDP, not for peer-to-peer applications.

## Collaborate

Are you excited about seeing low-level UDP in the browser? File an issue! Send a
PR! Get in contact with [@noffle](https://twitter.com/noffle)!
