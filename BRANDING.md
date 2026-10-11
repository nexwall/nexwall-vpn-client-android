# Nexwall VPN for Android (branded fork of ics-openvpn / "OpenVPN for Android")

Public, branded fork of [ics-openvpn](https://github.com/schwabe/ics-openvpn) by Arne Schwabe (GPLv2 with the
additional terms in `doc/LICENSE.txt`, which this fork keeps and follows: everything in the `de.blinkt.openvpn`
class hierarchy is a derivative work and stays GPLv2). It is the Android client for the SSL VPN (OpenVPN) of the
Nexwall firewall. The source of every released APK is this repository.

## Changes compared to upstream
- `applicationId` = `br.com.nexwall.vpn` (so it installs next to, and never replaces, the original app).
  The Kotlin/Java `namespace` stays `de.blinkt.openvpn` on purpose to keep merges with upstream cheap.
- App name "OpenVPN for Android" -> "Nexwall VPN" (English strings; attribution and credits are untouched).
- Launcher icons (legacy PNGs, adaptive icon foreground/monochrome vectors) and adaptive background colour.

## Build
`./gradlew assembleUiOvpn23Release` (JDK 25, Android SDK + NDK as in `.github/workflows/build.yaml`).
GitHub Actions builds on every push with debug signing (`icsopenvpnDebugSign=true`); release signing uses a
keystore that is NOT in this repository.

"OpenVPN" is a registered trademark of OpenVPN Inc.; Nexwall VPN is not affiliated with or endorsed by OpenVPN Inc.
