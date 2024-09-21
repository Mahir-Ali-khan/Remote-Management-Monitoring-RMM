# RMM Tools Used by Threat Actors

## Overview

This repository maintains a comprehensive list of Remote Monitoring and Management (RMM) tools that are exploited by various threat actors. As per the recent CrowdStrike Threat Hunting Report 2024, there is a rise in the usage of these tools for malicious purposes. This repository will maintain this list of all known RMM tools along with DNS queries made when executed, assisting in the hunt for these tools even if they are renamed or manipulated in any way.

Sigma rule available in this repository for creating hunt queries.

## Table of Contents

- [What are RMM Tools?](#what-are-rmm-tools)
- [Purpose of This Repository](#purpose-of-this-repository)
- [False Positives](#false-positives)
- [List of Known RMM Tools](#list-of-known-rmm-tools)
- [Sigma Rule](Remote-Management-Monitoring-RMM/Detect_RMM_Tool_Usage_via_DNS_Queries.yml)
- [Contributing](#contributing)
- [License](#license)

## What are RMM Tools?

Remote Monitoring and Management (RMM) tools allow IT professionals to manage and support devices and networks remotely. While these tools serve legitimate purposes, they can be misused by cybercriminals to gain unauthorized access.

## Purpose of This Repository

The goal of this repository is to:
- Provide a centralized list of RMM tools exploited by threat actors.
- Assist organizations in identifying and mitigating the use of compromised RMM solutions.

## False Positives

- Legitimate use of the tools needs to be excluded.
- All browser-based activity needs to be excluded.

## List of Known RMM Tools

| Sr. No | Tool Name                | Threat Group Usage                                                                                     | Common DNS Queries                                                            |
|--------|--------------------------|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| 1      | Action1                  | LockBit                                                                                            | *.action1.com                                                                |
| 2      | AeroAdmin                | Scattered Spider                                                                                  | *.aeroadmin.com                                                             |
| 3      | Ammyy Admin              | FIN7, APT28, Cobalt Group                                                                           | *.ammyy.com                                                                  |
| 4      | AnyDesk                  | Multiple Groups (BlackSuit, Royal, Akira, etc.)                                                   | *.net.anydesk.com                                                            |
| 5      | Atera                    | Multiple Groups (BlackSuit, Royal, AvosLocker, etc.)                                             | *.atera.com, agent.atera.com, portal.atera.com                              |
| 6      | Bomgar/BeyondTrust       | NA                                                                                                 | *.bomgar.com                                                                 |
| 7      | Chrome Remote Desktop     | Scattered Spider                                                                                  | remotedesktop.google.com                                                    |
| 8      | Domotz                   | Scattered Spider                                                                                  | *.domotz.com, *.domotz.co                                                   |
| 9      | DWAgent                  | Scattered Spider                                                                                  | *.dwservice.net, dwservice.net                                             |
| 10     | FixMe.IT                 | LockBit                                                                                            | fixme.it, *.techinline.net                                                  |
| 11     | Fleetdeck                | Scattered Spider                                                                                  | *.fleetdeck.io                                                              |
| 12     | GetScreen                | Scattered Spider                                                                                  | *.getscreen.me                                                               |
| 13     | GoTo (Logmein)          | Multiple Groups (BlackSuit, Royal, etc.)                                                           | *.gotoresolve.com, *.logmein.com, *.logmeinrescue.com, *.logmeininc.com   |
| 14     | JumpCloud                | NA                                                                                                 | *.jumpcloud.com                                                              |
| 15     | Level.io                 | Scattered Spider                                                                                  | *.level.io, *.twilio.com, realtime.ably.io                                   |
| 16     | MeshCentral              | Quantum Ransomware                                                                                  | meshcentral.com, *.meshcentral.com                                           |
| 17     | N-Able/BeAnywhere        | Scattered Spider                                                                                  | *.n-able.com, *.beanywhere.com, *.swi-rc.com, *.swi-tc.com, *.pubnub.com  |
| 18     | NetSupport               | Multiple Groups (Cuba, EvilCorp, Black Basta)                                                     | *.netsupportsoftware.com, *.netsupportmanager.com                           |
| 19     | Parsec                   | Scattered Spider                                                                                  | *.parsecgaming.com, *.parsec.app                                            |
| 20     | Pulseway                 | Scattered Spider                                                                                  | *.pulseway.com                                                              |
| 21     | Quick Assist             | Black Basta Ransomware                                                                              | remoteassistance.support.services.microsoft.com                              |
| 22     | RealVNC                  | Lazarus Group                                                                                       | *.tightvnc.com, update.tightvnc.com                                         |
| 23     | RemotePC                 | Scattered Spider                                                                                  | *.remotepc.com                                                               |
| 24     | RemoteUtilities          | RagnarLocker                                                                                        | *.remoteutilities.com                                                        |
| 25     | RustDesk                 | Akira                                                                                               | *.rustdesk.com, rustdesk.com                                               |
| 26     | ScreenConnect (ConnectWise Control) | Multiple Groups (Black Basta, BlackCat, LockBit, etc.)                                     | *.screenconnect.com, *.connectwisecontrol.com                               |
| 27     | SimpleHelp               | BlackCat                                                                                            | *.simple-help.com, simple-help.io                                            |
| 28     | Sorillus                 | Scattered Spider                                                                                  | *.sorillus.com                                                               |
| 29     | Splashtop                | Multiple Groups (Black Basta, LockBit, etc.)                                                      | *.splashtop.com, *.splashtop.eu                                            |
| 30     | Supremo                  | Black Basta                                                                                         | *.supremocontrol.com, *nanosystems.it                                      |
| 31     | TacticalRMM              | Multiple Groups (AvosLocker, Scattered Spider*)                                                   | *.tacticalrmm.io, *.tacticalrmm.com                                         |
| 32     | Tailscale                | Scattered Spider                                                                                  | *.tailscale.com                                                              |
| 33     | TeamViewer               | Multiple Groups (LockBit, BianLian, etc.)                                                         | *.teamviewer.com                                                             |
| 34     | Tmate                    | TeamTNT                                                                                             | *.tmate.io                                                                   |
| 35     | Twingate                | Scattered Spider                                                                                  | *.twingate.com, twingate.com, client.twingate.com                          |
| 36     | ZohoAssist               | LockBit                                                                                            | *.zoho.com, *.zohocdn.com, zohoassist.com                                   |


*Note: will update this list with any new RMM tools discovered, Please check back for new entries.*

## Contributing

We welcome contributions to this repository. If you know of additional RMM tools that should be included or have updates on existing entries, please follow these steps:

1. Fork the repository.
2. Create a new branch for your changes.
3. Add your entry to the list.
4. Submit a pull request.

Please ensure that any contributions follow the established format and provide reliable sources for claims regarding exploits or abuse.

Some RMM tools reference taken from [Ransomware Tool Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix).

## License

This repository is licensed under the [MIT License](LICENSE). Please feel free to use the information contained here for research and educational purposes.

## Disclaimer

This repository is intended for educational purposes only. The inclusion of any RMM tool does not imply endorsement or recommendation for use in malicious activities. Users are encouraged to employ good cybersecurity practices and conduct thorough research.

---

For questions or concerns, please open an issue in this repository.
