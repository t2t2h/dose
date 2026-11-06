# AflatoonMubdi
© AFLATOON | أفلاطون — exclusive to MUBDI

A single Theos project that builds one `AflatoonMubdi.dylib`. VPN / WireGuard / Packet Tunnel features have been removed completely. All remaining C, Objective-C, headers, image data, build configuration, and GitHub Actions workflow are kept together in this project root.

## Included modules
- `UI.m`, `Main.m`, `Hook.m` — menu, settings, and hook registration
- `Audio.c`, `DSP.c`, `Time.c` — audio processing and timing
- `DNS.c`, `Rebind.c`, `SpeedCore.c` — DNS, symbol rebinding, and in-process clock controls
- `Image.c` — embedded menu background image
- `Agora.m`, `AgoraStubs.h` — best-effort Agora integration
- Header files — shared declarations for the modules
- `Makefile` — one Theos dylib target
- `.github/workflows/build.yml` — GitHub Actions build

## Build
1. Upload the contents of this folder to the root of your GitHub repository.
2. Keep `.github/workflows/build.yml` at that exact path.
3. Open Actions and run **Build AflatoonMubdi**.
4. Download the artifact after the job succeeds.

## Notes
- The project produces one dylib; it is not an IPA or an independently installable app.
- `embedded-safe` disables runtime symbol hooks; features requiring runtime hooks will not be active in that mode.
- Jailbreak runtime hooks require a compatible ElleKit/libhooker environment already installed on the target device.
- Network tuning is limited to socket options in the target process; there is no VPN, tunnel, IP masking, or encryption feature.
- A successful CI compile still needs on-device compatibility testing.
