<div align="center">

# Hamachi App

**Download pages, version tracking and setup notes for Hamachi on Windows.**

[![Latest](https://img.shields.io/badge/current-2.4.0.79-00a86b?style=flat-square)](#)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%20%2F%2011-0078D4?style=flat-square&logo=windows&logoColor=white)](#)
[![Installer](https://img.shields.io/badge/installer-MSI-6e7681?style=flat-square)](#)
[![Checksums](https://img.shields.io/badge/checksums-SHA--256-8957e5?style=flat-square)](#)

</div>

---

### What this account publishes

| Repository | What's inside |
|---|---|
| **[hamachi-download](https://github.com/hamachi-app/hamachi-download)** | Version tracking, SHA-256 checksums and install notes for the Windows MSI |

### Why

Hamachi's download page is a single button with no checksum and no version on it. This account keeps the boring parts in version control: which build is current, what its hash is, how to install it silently, and when it last changed.

- Version is read from the installer's own `ProductVersion` resource, not guessed.
- Checksums are recomputed against the vendor CDN, not copied from forums.
- Every download link points to LogMeIn's own endpoints — nothing is re-hosted.

### Quick reference

```powershell
# download
Invoke-WebRequest https://secure.logmein.com/hamachi.msi -OutFile hamachi.msi

# verify
Get-FileHash .\hamachi.msi -Algorithm SHA256
# 5c672c9a12b69b75b2cf25710bac8c579b3ef7ed1a907930dc0d7e20eab7584d

# silent install
msiexec /i hamachi.msi /qn
```

---

<div align="center">
<sub>Version tracked from the installer's own <code>ProductVersion</code> resource.</sub>
</div>
