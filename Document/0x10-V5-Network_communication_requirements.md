# V5: Network Communication Requirements

## Control Objective

The purpose of the controls listed in this section is to ensure the confidentiality and integrity of information exchanged between the mobile app and remote service endpoints. At the very least, a mobile app must set up a secure, encrypted channel for network communication using the TLS protocol with appropriate settings. Level 2 lists additional defense-in-depth measure such as SSL pinning.

## Security Verification Requirements

| # | MSTG-ID | Description | L1 | L2 |
| --- | --- | --- | --- | --- |
| **5.1** | MSTG‑NETWORK‑1 | Data is encrypted on the network using TLS. The secure channel is used consistently throughout the app. | ✓ | ✓ |
| **5.2** | MSTG‑NETWORK‑2 | The TLS settings are in line with current best practices, or as close as possible if the mobile operating system does not support the recommended standards. | ✓ | ✓ |
| **5.3** | MSTG‑NETWORK‑3 | The app verifies the X.509 certificate of the remote endpoint when the secure channel is established. Only certificates signed by a trusted CA are accepted. | ✓ | ✓ |
| **5.4** | MSTG‑NETWORK‑4 | The app either uses its own certificate store, or pins the endpoint certificate or public key, and subsequently does not establish connections with endpoints that offer a different certificate or key, even if signed by a trusted CA. |   | ✓ |
| **5.5** | MSTG‑NETWORK‑5 | The app doesn't rely on a single insecure communication channel (email or SMS) for critical operations, such as enrollments and account recovery. |  | ✓ |
| **5.6** | MSTG‑NETWORK‑6 | The app only depends on up-to-date connectivity and security libraries. |  | ✓ |

## References

The OWASP Mobile Security Testing Guide provides detailed instructions for verifying the requirements listed in this section.

- Android - <https://github.com/OWASP/owasp-mstg/blob/master/Document/0x05g-Testing-Network-Communication.md>
- iOS - <https://github.com/OWASP/owasp-mstg/blob/master/Document/0x06g-Testing-Network-Communication.md>

For more information, see also:

- OWASP Mobile Top 10: M3 (Insecure Communication) - <https://www.owasp.org/index.php/Mobile_Top_10_2016-M3-Insecure_Communication>
- CWE 319 (Cleartext Transmission of Sensitive Information) - <https://cwe.mitre.org/data/definitions/319.html>
- CWE 295 (Improper Certificate Validation) - <https://cwe.mitre.org/data/definitions/295.html>
