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

