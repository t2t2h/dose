# AflatoonMubdi — implementation notes

The project is a single Theos dylib target. All VPN / WireGuard / Packet Tunnel code and UI have been removed at the user's request.

## Audio behavior
- Microphone processing assumes AudioUnitRender capture bus 1.
- Incoming playback processing assumes bus 0.
- These assumptions are app/audio-stack dependent; they are not a universal VoIP hook.
- Agora integration is best-effort Objective-C selector swizzling, not a native raw-frame delegate.

## Network behavior
- DNS overrides are scoped to calls intercepted in the target process.
- Socket tuning changes selected TCP socket options; it does not reduce server ping or create a tunnel.

## Build status
The GitHub Actions workflow validates source/header presence and compiles the Theos library. A successful build and real-device testing are required before treating the artifact as verified.
