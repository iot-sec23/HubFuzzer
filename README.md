# HubFuzzer

## Introduction 
This repository was created for the project "No More Companion Apps Hacking but One Dongle: Hub-Based Blackbox Fuzzing of IoT Firmware".

## Research Paper
This work is published on MobiSys'23 [Link](https://www.sigmobile.org/mobisys/2023/accepted-papers.html).
If you use `HubFuzzer` in a scientific publication, we would appreciate citations using this **Bibtex** entry:
```
@inproceedings{ma2023nomore,
  title={No More Companion {Apps} Hacking but One Dongle: {Hub-BasedBlackbox} Fuzzing of {loT} Firmware},
  author={Ma, Xiaoyue and Zeng,Qiang and Chi, Haotian and Luo, Lannan},
  booktitle={In Proc. ACM International Conference on Mobile Systems, Applications, and Services (MobiSys)},
  year={2023}
}
```
## Repository structure
The code is currently being organized and will be made available soon.

## Abstract
Given the massive difficulty in emulating IoT firmware, blackbox fuzzing of IoT devices for vulnerability discovery has become an attractive option. However, existing blackbox IoT fuzzers need much time and tedious effort to reverse engineer the IoT companion app (or manually collect test scripts) of each IoT device, which is unscalable when analyzing many devices. Moreover, fuzzing through a companion app is impeded by the input sanitization inside the app and limited to the manually revealed functions. We notice that IoT devices are typically able to connect a hub using standard wireless protocols (such as ZigBee, Z-Wave, and WiFi). We thus propose a uniform hub-based architecture for fuzzing various IoT devices, without reverse engineering any companion apps. It exploits the messages exchanged between a hub and an IoT device to automatically discover all the functions, and then launches systematic function-oriented message-semantics-guided fuzzing. It avoids sanitization imposed by a companion app. In addition, it conducts device state-sensitive fuzzing, which we find very effective in finding IoT bugs. We implement the system named HubFuzzer. The evaluation shows that HubFuzzer leads to much higher coverage than prior state of the art. We test 21 IoT devices and find 23 zero-day vulnerabilities. Four CVEs have been assigned.

## Vulnerablity Discovery

|Device Name|	Device ID|	Number of Vulnerabilities|	CVE Allocation|
|---------------|------|-------|--------------|
|Centralite Pearl|	1|	2	|[CVE-2023-24678](https://nvd.nist.gov/vuln/detail/CVE-2023-24678)|
|Sengled Bulb E11-N1EAW|	2|	8|	[CVE-2022-47100](https://nvd.nist.gov/vuln/detail/CVE-2022-47100)|
|Sengled Strip E1G-G85|	5	|8	|[CVE-2022-47100](https://nvd.nist.gov/vuln/detail/CVE-2022-47100)|
|Third Reality 3RSB015BZ|	6|	2|	[CVE-2023-29780](https://nvd.nist.gov/vuln/detail/CVE-2023-29780)|
|Sengled E1E-G7F	|13|	1	|[CVE-2023-29779](https://nvd.nist.gov/vuln/detail/CVE-2023-29779)|
|Aeotec ZW130-A	|15	|1	|Under Review |
|Fibaro FGMS-001	|18	|1	|Under Review |

## License

GNU General Public License v3.0

