> Official Live Page: https://xaynxai.com/device-tracker-policy

Effective Date: November 16, 2026 • Version 1.0

# Device tracker policy

This Device Tracker Security, Privacy, and Terms Policy ("Policy") outlines the operational principles, geographic location processing standards, cryptographic hardware protections, and legal user responsibilities for the **Device Tracker**service operated by Xaynx AI Teknoloji ("Company", "we", "us", or "our").

**Zero-Knowledge & End-to-End Encryption (E2EE) Architecture:** Your location coordinates and hardware telemetry are encrypted client-side using 256-bit AES-GCM before leaving your browser. Xaynx AI's proprietary secure server infrastructure and isolated databases store only cryptographic ciphertext. The decryption key is never transmitted to our servers and remains isolated strictly inside the URL hash (#) fragment.

---

## 1. Privacy Policy: Processing of Location & Device Data

Our service processes the following hardware telemetries solely to visualize your device's physical coordinates on the map and facilitate emergency recovery:

- **Geographic Coordinates:** Latitude, longitude, altitude above sea level, heading angle, movement speed, and accuracy radius formatted in WGS-84 standard.
- **Device & Hardware Telemetry:** Operating system platform (macOS, Windows, iOS, Android, Linux), browser engine, CPU core counts, screen dimensions, and battery percentage via the Battery Status API.
- **Network & Connectivity State:** Online/offline connectivity flag, network round-trip time (RTT), and effective connection type (WiFi, cellular, or ethernet).

None of this data is ever shared with advertising networks, commercial data brokers, or Xaynx AI's remote backend servers. All coordinate evaluations and distance calculations (Haversine formula) execute strictly client-side.

---

## 2. Location Tracking Policy: Real-Time GPS Operation

Our platform **strictly prohibits the use of simulated, mock, or synthetic demo coordinates**. Live tracking operates exclusively through a multi-tier physical hardware acquisition pipeline:

- **Tier 1 - High Accuracy Hardware GNSS:** Direct queries query the onboard GNSS/GPS chipset or OS CoreLocation framework (enableHighAccuracy: true) providing 3 to 15 meter precision upon satellite lock.
- **Tier 2 - Wi-Fi Triangulation & Hybrid Mode:** On laptops or indoor spaces lacking line-of-sight satellite reception, the tracker seamlessly triangulates nearby Wi-Fi access beacons without UI stutter.
- **Tier 3 - Physical Network (IP) Verification:** If OS-level permissions face latency or driver locks, the user can affirmatively trigger real-world coordinates via their modem's physical network IP address.

---

## 3. Terms of Use: Rules & User Responsibilities

Every individual initializing the Device Tracker or generating tracking links agrees unconditionally to the following enforceable rules of conduct:

- **Exclusive Ownership or Documented Authority:** The utility may only be activated on hardware personally owned by the user or for which explicit, lawful written tracking authority has been granted.
- **Strict Prohibition of Covert Surveillance & Stalking:** Secretly monitoring third parties without affirmative written consent constitutes illegal surveillance and stalking under applicable criminal statutes.
- **Misuse of Emergency Acoustic & Lock Features:** High-decibel acoustic sirens and screen lock overlays are strictly intended for physical recovery of misplaced hardware. Any abusive disruption or harassment is forbidden.

---

## 4. Data Retention & Deletion Policy: Location History & Disposal

The lifecycle and permanent erasure policies governing breadcrumb history and location caches are detailed below:

- **200-Point FIFO Local Buffer:** A maximum of 200 consecutive breadcrumb points are maintained in local memory. Upon the 201st fix, the oldest coordinate is permanently purged.
- **Isolated LocalStorage Domain:** Location trails reside strictly under private origin-scoped LocalStorage keys. No third-party domain, browser extension, or external entity can inspect this storage.
- **Instant One-Click Permanent Purge:** Clicking the 'Clear Trail' button instantly and irreversibly overwrites and empties all coordinate buffers and cached telemetry.

---

## 5. Permissions & Consent Policy: Hardware Access & User Control

The Device Tracker respects explicit, transparent browser consent mechanisms before engaging any hardware sensors:

- **Mandatory User Authentication Gate:** The Device Tracker is strictly restricted to authenticated Xaynx AI account holders. Unauthenticated visitors are barred from invoking GPS sensors, viewing maps, or transmitting telemetry, with DOM-level enforcement redirecting to secure login.
- **Pre-Conditioned Onboarding & Affirmative Consent:** Before the user explicitly reviews and ticks the affirmative consent checkbox on the initial onboarding screen, no hardware permissions are requested and zero background network calls are initiated.
- **Explicit Geolocation Consent:** No coordinate polling initiates unless the user positively clicks 'Allow' on the native browser security dialog.
- **User-Initiated Acoustic Authorization:** Browser autoplay security policies ensure the acoustic siren synthesizer can never play automatically or covertly without an explicit physical click.
- **Instant Revocation of Consent:** Users can revoke permissions at any moment via the address bar lock icon, which immediately halts all watchPosition telemetry streams.

---

## 6. Security Policy: Cryptographic Protection Against Unauthorized Access

Device telemetry and live tracking links are guarded by military-grade cryptographic primitives:

- **256-Bit Cryptographic Randomness:** Device tracking keys and session tokens are generated utilizing Web Crypto API (crypto.getRandomValues) hardware entropy, preventing collision and brute-force guessing.
- **Hash-Fragment Protocol Isolation (RFC 3986):** Access keys reside strictly inside the URL hash fragment (#), which standard HTTP RFC 3986 specifications prevent from ever transmitting to servers or intermediary proxies.
- **One-Way SHA-256 PIN Hashing:** Your Lock Mode screen PIN is never saved in plaintext; only its one-way SHA-256 cryptographic digest is verified in volatile memory.
- **Remote Lost Mode & Emergency Notice:** Device owners can remotely invoke full-screen lock banners displaying secure recovery instructions and optional contact phone numbers, dismissible via dashboard or PIN.
- **Dynamic Geofence Boundary Shield:** Users can establish a virtual safe zone (100m–1000m). Exiting the boundary immediately triggers client-side Haversine breach alerts.
- **Hardware Keep-Alive & Standby Mitigation:** To prevent OS sleep states from suspending telemetry streams, native Screen WakeLock APIs and client-side audio loops operate strictly during active sessions without intrusive software.

---

## 7. Children's Privacy Policy (COPPA & GDPR-K Compliance)

The safety, physical protection, and digital privacy of minors is an absolute priority:

- **Mandatory Custodial Supervision:** Tracking devices used by minors under 18 years of age is strictly permitted solely under the affirmative oversight and consent of legal guardians.
- **Zero Profiling & Commercial Exploitation Ban:** No minor location records are ever gathered, analyzed, profiled, or sold for marketing, behavioral tracking, or commercial gain.
- **Strict Liability for Unauthorized Minor Tracking:** Installing tracking tools on the hardware of minors without lawful parental custody is severely penalized under international child protection laws.

---

## 8. Account & Data Deletion Policy: Permanent Digital Erasure

Users retain unconditional control to permanently purge all device identifiers and telemetry at will:

- **Immediate Dashboard Purge:** Clicking 'Clear Trail' inside the device card instantly erases the entire current breadcrumb trail from browser cache.
- **Cryptographic Identifier Decommissioning:** Clearing site storage or cookies inside browser settings permanently destroys the random XY- device token, leaving no recoverable lineage.
- **Zero Server Residue Guarantee:** Because no coordinates or device profiles ever enter remote databases, clearing local browser memory guarantees complete 100% digital annihilation.

---

## How to Contact Us

If you have inquiries regarding our Device Tracker security protocols, hardware compliance, or this policy, please reach out to our Compliance & Privacy Team:

[contact@xaynx.co m](mailto:contact@xaynx.co m)

Xaynx AI Teknoloji A.Ş. • Device Security & Cryptography Unit
