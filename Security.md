# Security Policy / Política de Seguridad

**ParanoidCrypto** · DNA-based text encryption  
Author: Paris Lavin · ORCID: [0000-0002-8893-526X](https://orcid.org/0000-0002-8893-526X)  
Website: [https://www.paranoidcrypto.cl](https://www.paranoidcrypto.cl)

---

## 🌐 Languages / Idiomas

- [English](#english)
- [Español](#español)
- [Português](#português)

---

<a name="english"></a>
## 🇬🇧 English

### Supported Versions

| Version | Supported          |
| ------- | ------------------ |
| 1.0.x   | ✅ Supported       |
| < 1.0   | ❌ Not supported   |

### Reporting a Vulnerability

If you discover a security vulnerability in ParanoidCrypto, please help us by reporting it responsibly.

**DO NOT open a public issue** for security vulnerabilities.

#### How to report

1. **Email**: Contact the author via ORCID: [0000-0002-8893-526X](https://orcid.org/0000-0002-8893-526X)
2. **Include**:
   - Description of the vulnerability
   - Steps to reproduce
   - Potential impact
   - Suggested fix (if any)
3. **Expected response time**: 48-72 hours
4. **What to expect**:
   - Acknowledgment of your report
   - Regular updates on progress
   - Credit in the security advisory (unless you prefer to remain anonymous)

### Security Architecture

#### Client-Side Processing

ParanoidCrypto is designed with privacy as a core principle:

- ✅ **All encryption/decryption happens in the user's browser**
- ✅ **No data is sent to external servers** (except the visitor counter)
- ✅ **No backend processing** of user content
- ✅ **Secret keys never leave the user's device**
- ✅ **No cookies or tracking** of user activity

#### Cryptographic Implementation

| Component | Implementation | Notes |
|-----------|----------------|-------|
| SHA-256 | Pure JavaScript | Based on FIPS 180-4 standard |
| XOR Cipher | Symmetric stream cipher | Uses SHA-256-derived keystream |
| Key derivation | SHA-256 + counter mode | Generates pseudo-random stream |
| DNA encoding | 2-bit to nucleotide mapping | `00→A`, `01→T`, `10→G`, `11→C` |

#### Firebase Integration

The visitor counter uses Firebase Realtime Database:

- Only stores anonymous visit counts and visitor IDs
- No personal data is collected
- Visitor IDs are randomly generated and stored locally
- Rules must be configured properly (see below)

### Firebase Security Rules

For production use, configure these rules in your Firebase Realtime Database:

```json
{
  "rules": {
    "site_stats": {
      "total_visits": {
        ".read": true,
        ".write": true
      },
      "visitors": {
        "$visitor_id": {
          ".read": true,
          ".write": true
        }
      }
    }
  }
}