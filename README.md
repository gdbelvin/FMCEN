# Find My Contact Event Numbers (FMCEN)
A privacy preserving protocol for contact tracing

[Design Document](https://docs.google.com/document/d/1jFOic0--h1Le5x44iwj3jY0k23nUuEL9gGgPSE0H-hs/edit#heading=h.xqo0gbx2v7i4)

## Status

Other simpler protocols offer more privacy

- [PACT](https://pact.mit.edu/wp-content/uploads/2020/04/The-PACT-protocol-specification-ver-0.1.pdf)

### Comparison

- **Server Privacy** An honest-but-curious server should not learn information about any user's location or contacts.
- **Source Integrity** Users cannot send reports to users they did not come in contact with or on behalf of other users.
- **Broadcast Integrity** Users cannot broadcast CENs they did not generate.
- **No Passive Tracking** A passive adversary monitoring Bluetooth connections should not be able to learn any information about the location of users who do not send reports.
- **Receiver Privacy** Users who receive reports do not reveal information to anyone.
- **Reporter Privacy** Users who send reports do not reveal information to users they did not come in contact with, and reveal only the time of contact to users they did come in contact with.

|Property                | PACT | FMCEN
|------------------------|------|--------|
|**Compatible with FindMy**|🟡  | ✅    |
|**Server Privacy**      | ✅   | ❌ Server learns contacts that have proximity for over x days |
|**Source Integrity**    | ✅   | ✅    |
|**Broadcast Integrity** | ✅   | 🟡 Could be prevented with 64 bytes for a signature |
|**No Passive Tracking** | ✅   | ✅    |
|**Receiver Privacy**    | ✅   | 🟡 Users reveal the k anonymity of contact matches |  
|**Reporter Privacy**    | ❌   | ✅    |
| - **Private Health Records**| ❌ | ✅  |
| - **Private Location History**| ❌ | ✅|




