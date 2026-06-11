# Third-Party Notices

Cove relies on third-party software in two distinct ways. This document covers
both.

> **Not legal advice.** The license identifiers below are provided for
> transparency and are accurate to the best of our knowledge, but licenses
> change between versions. Always verify against the exact version distributed
> to you, and consult a professional before commercial distribution —
> especially for the copyleft components flagged below.

---

## 1. Managed components (downloaded, not bundled)

Cove **downloads** the tools below from their **official upstream sources** at
the user's request and runs them locally. Cove does **not** bundle, embed, or
re-host these binaries; the package registry publishes only manifests (download
URLs and integrity hashes) pointing at the official upstreams. As such, Cove
acts as a downloader/manager (similar to a package-manager front end) rather
than a redistributor.

Each component remains subject to its own license. Users are responsible for
complying with the license of any component they choose to install and use.

| Component | Typical license | Notes |
| --- | --- | --- |
| PHP | PHP License v3.01 | Permissive |
| Node.js | MIT (with bundled deps) | Permissive |
| Composer | MIT | Permissive |
| Caddy | Apache-2.0 | Permissive |
| Nginx | BSD-2-Clause | Permissive |
| Apache HTTP Server | Apache-2.0 | Permissive |
| PostgreSQL | PostgreSQL License | Permissive (BSD/MIT-like) |
| Memcached | BSD-3-Clause | Permissive |
| Meilisearch | MIT | Permissive |
| Mailpit | MIT | Permissive |
| MailHog | MIT | Permissive |
| Erlang/OTP | Apache-2.0 | Permissive |
| mkcert | BSD-3-Clause | Permissive (local CA tooling) |
| RabbitMQ (server) | MPL-2.0 / Apache-2.0 | Weak (file-level) copyleft |
| Adminer | Apache-2.0 **or** GPL-2.0 (dual) | Choose a license at use |
| MySQL (Community) | GPL-2.0 (+ FOSS Exception) | ⚠ Copyleft |
| MariaDB (server) | GPL-2.0 | ⚠ Copyleft |
| phpMyAdmin | GPL-2.0 | ⚠ Copyleft |
| HeidiSQL | GPL-2.0 | ⚠ Copyleft |
| Redis | BSD-3-Clause (≤ 7.2) · RSALv2 / SSPL-1.0 (7.4+) | ⚠ Verify by version |
| MongoDB (Community) | SSPL-1.0 | ⚠ Strong (network) copyleft |
| MinIO | GNU AGPL-3.0 | ⚠⚠ Strong network copyleft |

**Compliance flags.** The ⚠ items carry obligations that can extend to anyone
who distributes or offers them as a network service. Because Cove downloads
these from upstream rather than redistributing them, the obligations generally
fall on the end user who installs and operates them — but if you ever bundle,
re-host, or offer these as a hosted service, review each license (particularly
**MinIO/AGPL**, **MongoDB/SSPL**, **MySQL/MariaDB/GPL**, **Redis/SSPL**)
carefully.

---

## 2. Components built into Cove

Cove itself is compiled from open-source libraries:

- **Rust crates** (backend) — predominantly MIT and Apache-2.0, plus
  permissive licenses such as BSD, ISC, Zlib, Unicode-3.0, MPL-2.0, and
  CDLA-Permissive-2.0.
- **npm packages** (frontend) — predominantly MIT, with Apache-2.0 and other
  permissive licenses.

The full, generated list of these components and their license identifiers is
shipped inside the application under **Settings → About** (sourced from
`src/lib/licenses.json`). No copyleft license that would impose obligations on
Cove's own proprietary distribution is present in this set.

---

_This file lists license identifiers only. Full license texts are available
from each project's official repository and are included with the respective
downloaded component._
