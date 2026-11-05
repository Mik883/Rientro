# Compatibility and test status

[Italiano](../COMPATIBILITA.md) · **English** · [Setup guide](GUIDE.md)

A selectable brand or family does not certify every model. New direct connector
paths have software/simulated-response tests, not universal physical validation.

| Component | Route | Status / limits |
| --- | --- | --- |
| Windows x64 | Setup and portable 2.0.1 | Compiled, runtime and interface verified; unsigned Windows EXEs |
| Android | Signed 2.0.1 APK | Build, lint and public signing identity verified; physical upgrade still requires testing |
| Home Assistant | Selected entities and device_tracker presence | Optional; development-home arrival flow tested |
| Tenda MX | Authenticated client list | Existing path retained; check model/firmware |
| FRITZ!Box | TR-064 Hosts | Software tests; real-model check required |
| OpenWrt | ubus/hostapd | Software tests; authorized access to all relevant APs required |
| WINDTRE / Vodafone / Sky / TIM | Actual supported TR-064/ubus protocol | Model/firmware required; no generic brand compatibility claim |
| ARP | Diagnostics | Not an operational arrival source |
| BTicino / Ajax direct | Unofficial cloud connectors | Accounts, 2FA, firmware and external services must be checked |
| Shelly dry contact | Recognized Gen1/RPC models | Reading/pulse software tests; verify wiring and actual model |
| Sonoff dry contact | iHost/eWeLink CUBE API v2, verified OFF inching | Compatible gateway/device required; simulated tests |
| Nuki | Compatible HTTP Bridge | Software tests; not every Nuki generation |
| Tedee | Local Bridge API | Software tests; Bridge needs Internet for certificates |
| SwitchBot direct | Lock/Lock Pro encrypted BLE | Keys and local Bluetooth required; other direct BLE generations not claimed |
| SwitchBot through Home Assistant | Compatible HA lock entity | Depends on the selected HA integration/model; distinguish lock/unlock/unlatch capabilities |
| iPhone / iPad | Web app, trusted HTTPS | Real installation and notifications still require testing |
| macOS | No binary included | Separate Mac compilation/testing required |

No physical gate position is claimed without a sensor. Read errors do not mean
certain absence. Unofficial cloud APIs can change independently of Rientro.
