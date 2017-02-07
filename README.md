# Web UDP
> Experiment for a web standard for creating and using UDP sockets in the browser.

*(More coming soon!)*

## What?

- a low level browser api granting access to UDP sockets

## Why?

- webrtc is too heavy on resources
  - can open very few connections /wo overloading machine
- webrtc is too heavy on implementation
  - lack of non-chrome / non-ff implementations due to complexity
  - too heavy to easily talk to embedded machines
- these result in webrtc being ineffective for many interesting and exciting
  applications (peer-to-peer apps; bittorrent; real-time games)

## How?

- xor /w random nonce to scramble payload, to prevent web-udp sites from being
  attacking non-web-udp services /wo explicitly supporting web-udp

## Implementation Vectors

No implementation exists yet, but there are a few different options:

- Chrome App: these provide [a UDP API](https://developer.chrome.com/apps/sockets_udp)
  - Google has [decided to nix Chrome Apps](https://blog.chromium.org/2016/08/from-chrome-apps-to-web.html)
- [Beaker Browser](https://github.com/beakerbrowser/beaker): integrate natively
- Fork Chromium and write an implementation

## Collaborate

Are you excited about seeing low-level UDP in the browser? File an issue! Send a
PR! Get in contact with [@noffle](https://twitter.com/noffle)!
