### SystemReady-IR-Workshop

##### Environment

Toybrick TB-RK3588X (https://armkeil.blob.core.windows.net/developer/Files/pdf/certificate-list/arm-systemready-ir-certification-rockchip.pdf) <br>
ArmSoM Sige7 (https://armkeil.blob.core.windows.net/developer/Files/pdf/certificate-list/arm-systemready-ir-certification-armsom.pdf) <br>

- Arm SystemReady IR 2.0

--> The newest reference software/firmware stack

- Trusted Firmware-A v2.10.0
- U-Boot 2024.07
- openSUSE Tumbleweed 20240808 (Linux Kernel 6.10.3)
- Fedora Server 41 (Linux Kernel 6.11.0-rc3)

--> Applications "just works" on different OSes

- demo0: Hardware/Firmware "just works"
    - UEFI, Devicetree, SMBIOS, FFA, PSCI, SCMI components
    - libubootenv, dmidecode, fwts, hwcaps

- demo1: LLM "just works"
    - git clone, compile and run: an easy/useful LLM chatbot (llama.cpp + Qwen2 1.5b)
    - cpufreq enabled: significant performance improvement
        - `cpupower -c all frequency-set -g performance`

- demo2: NAS "just works"
    - Rockstor, CasaOS, Cockpit
