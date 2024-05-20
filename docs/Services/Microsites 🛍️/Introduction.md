---
stoplight-id: c5u2vshxbdks7
---

# Introduction

The Placetopay Microsites API enables the creation and management of microsites. These microsites can be either open or closed and are designed for specific users of the microsites API. The API offers a robust and secure interface for creating, authenticating, and managing microsites.

## Authentication

To interact with the Microsites API, service authentication credentials are required. The authentication parameters are as follows:

- **login**: Site identifier.
- **tranKey**: Transactional key generated using the formula Base64(SHA-1(nonce + seed + secretkey)). The nonce field must be in its original format (not Base64 encoded).
- **nonce**: Random value encoded in Base64.
- **seed**: Current date in ISO 8601 format.

## Contact

For more information, please contact the Placetopay support team.

---

This documentation provides an overview of the main features and authentication requirements of the Placetopay Microsites API. For complete details, please refer to the full API specification.
