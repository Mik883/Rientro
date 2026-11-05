# Installation and configuration

[Italiano](../GUIDA-PRIMO-AVVIO.md) · **English** · [Back to the project](../../README.en.md)

## Windows

Use Windows 10/11 x64 and Microsoft Edge WebView2. Download the setup or extract
the portable archive completely, then start `Rientro.exe`. Do not run it inside
the ZIP. Windows executables are not commercially Authenticode-signed; check the
official download and SHA-256 checksum before deciding whether to proceed.

The PC must remain on and the service must keep running. The configuration
window need not stay in the foreground. Sleep or shutdown interrupts operation.
Verify startup after signing in to Windows following a reboot; do not assume
another household's startup configuration exists on a new installation.

The public data profile is `%USERPROFILE%/RientroData/Public`. Portable does not
mean encrypted credentials can be moved between PCs: Windows DPAPI credentials
are bound to their Windows context.

## Household and connectors

The interface is currently in Italian. Open **Connettori** (Connectors) and choose
Home Assistant or direct integrations. For Home Assistant, configure its local
URL and an authorized access token, verify the connection and explicitly select
the entities. Never publish that token. Gate and smart-lock entities must differ.

Direct routes include the documented BTicino/Ajax connectors, supported Shelly
dry-contact relays, Sonoff through an appropriate iHost/eWeLink CUBE gateway,
and supported Nuki, Tedee or SwitchBot lock paths. These are specific protocols,
not universal support for every brand model. Cloud-backed direct routes still
need Internet and manufacturer accounts; “direct” does not mean offline.

For a gate relay, use a dedicated opening input and the documented pulse mode,
not an arbitrary toggle output. Configure safe OFF/inching behavior. Without a
position sensor, the program cannot confirm the physical gate position.

In **Rientro** (Arrival), choose the authorized actions, order and delays before
each step. Actions occur only after confirmation. If an alarm is configured,
the door must follow confirmed disarming. Saving settings and discovering devices
do not issue physical commands. The unlock-and-unlatch operation requires device
support; an uncertain result is not automatically retried.

## Presence and router

In **Impostazioni** (Settings), choose the presence source independently from
the actuator connectors:

| Source | Required configuration |
| --- | --- |
| Supported Tenda MX | Authenticated client-list access |
| FRITZ!Box | Local IP, authorized account, enabled TR-064 |
| OpenWrt | Local IP, ubus credentials, access to all relevant hostapd APs |
| Home Assistant | Supported device_tracker entities bound to the right people |
| WINDTRE, Vodafone, Sky, TIM | Exact model, firmware and an available supported protocol; brand alone is insufficient |
| ARP | Diagnostics only; does not enable operational arrival detection |

Discover devices, then explicitly associate each phone with a person. Use the
phone's actual MAC for the home Wi-Fi network, including its private/randomized
MAC if enabled for that network. Discovering an IP alone is not proof of identity.
Configure minimum absence and stable reconnection times; a failed router reading
must not be treated as certain absence.

## Android and pairing

1. Install the signed `Rientro-2.0.1.apk` from the official release. Android may
   require temporary permission to install from your chosen source.
2. Configure mobile HTTPS access in the Windows program. Generate a one-time
   pairing code for that specific phone.
3. In the app, enter the household's HTTPS address and pairing code before it expires.
4. Allow notifications and enable the background connection. Run the notification
   test, press Home and verify that tapping the notification opens Rientro.
5. After a force-stop, reopen the app and reactivate the connection. Vendor battery
   restrictions can affect delivery. Connection and arrival notifications are separate.

The APK alone is insufficient: your household's Windows service must be configured
and reachable. This is direct APK distribution, not a Google Play listing.

## Local and remote access

At home, use the configured local route. Away from home, install and configure
Tailscale on the PC and phone, authorize access to that private network and set
up Tailscale Serve HTTPS to the configured local Rientro service. Do not expose
the service with Funnel or public router port forwarding as part of this setup.
Tailscale is a separate service with its own terms and limits.

Rientro does not provide a hosted relay or mandatory household registration.
Web push and cloud integrations may still contact their respective external
services. Local operation does not mean every connector works without Internet.
Being able to view the app remotely does not grant permission to open the gate:
the configured fresh-presence and one-time confirmation checks still apply.

## iPhone and iPad

Use your own household's trusted HTTPS address. Safari does not automatically
trust the Android LAN transport certificate. Open the address in Safari, pair
the device, choose **Share → Add to Home Screen → Add**, reopen from the new icon
and grant notifications where supported. Test delivery before physical commands.

There is no universal web-app URL for all homes and no native iOS app in this release.
Sending a link and code to a phone on mobile data does not make a LAN-only backend
reachable. The web-interface ZIP is not a standalone backend. Real iOS/iPadOS
installation and notification tests remain to be completed for this distribution.

## Users and administrators

Each phone has its own pairing
and session; do not share them between people. In **Dispositivi** (Devices), add
the name and home-network MAC, generate a pairing code and send it privately.
Expired codes must be regenerated. In **Impostazioni → Amministratori dell’app**,
explicitly authorize the phones allowed to configure the household.

Other users retain only their authorized capabilities. If a phone is lost or
replaced, revoke its association and pair the replacement.

## Maintaining your installation

Back up `%USERPROFILE%/RientroData/Public` before replacing program files.
Stop Rientro, run the official setup or extract the complete portable archive,
and preserve the data profile. Keep Android installed when installing an official
APK signed with the same identity. Changing the HTTPS origin may require pairing
again. Configure Tailscale on the PC and phone for access outside the home network.

## Testing and limits

The release passed 229 software tests, with one skipped, and desktop/mobile
interface checks. This is not universal hardware certification. New rules must
be explicitly enabled. Verify device status and notifications first; supervise
the first physical commands. Socket/climate bindings do not imply universal
commands are implemented. Light automations currently use Home Assistant.

See the [compatibility matrix](COMPATIBILITY.md). macOS binaries and native iOS
apps are not included. Do not rely on this software as your only physical access
or as a replacement for certified alarm or emergency systems.

## Security and support

Issues and compatibility reports are welcome in Italian or English. Include
version, exact model/firmware, redacted steps and observed result. Do not post
tokens, pairing codes, private keys, profiles, databases or unredacted home data.
For vulnerabilities, contact **mikelean@hotmail.it** privately, subject
**Rientro — security**. No emergency response or guaranteed support period is offered.

Rientro is free proprietary software, not open source. Read the
[English licence translation](../../LICENSE.en.txt) and [third-party notices](THIRD-PARTY.md).
