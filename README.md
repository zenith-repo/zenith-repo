<h3 align="center">zenith-repo</h3>
<p align="center"><code>music distribution plumbing</code> · <code>DDEX standards</code> · <code>onchain royalty settlement</code></p>

<p align="center">
  <a href="https://github.com/zenith-repo?tab=repositories"><img src="https://img.shields.io/badge/Repos-15-2f81f7?style=flat&logo=github&logoColor=white" alt="repos" /></a>
  <a href="https://github.com/zenith-repo?tab=followers"><img src="https://img.shields.io/badge/Followers-follow-8957e5?style=flat&logo=githubsponsors&logoColor=white" alt="followers" /></a>
  <img src="https://img.shields.io/badge/Status-Building-3fb950?style=flat&logo=statuspage&logoColor=white" alt="status" />
</p>

---

### The delivery spine meets the settlement layer

I work on the unglamorous middle of the music business: the part that turns a finished master into a
statement a rights-holder can actually be paid against. That means DDEX — ERN on the way out, DSR on the
way back — and it means treating a royalty statement as the source of truth rather than something an
oracle guesses at.

The work splits into three layers. First, the **delivery spine**: ERN generation, DSP-side receiving,
ERN/DSR parsing and validation, then statement ingest and reconciliation. Second, the **contract layer**:
royalty splits, a vetted contract library, transfer-restricted security tokens for revenue-bearing
instruments, creator coins, and an AMM. Third, the **data surface**: a read-only catalogue API for
royalty and release metadata.

Two design convictions run through all of it. A revenue-bearing token is a security, so transfer
restrictions are not a feature to add later. And per-stream on-chain settlement is arithmetically
impossible — aggregation is the only thing that scales, so revenue lands in epochs against a
Merkle root rather than one transaction per play.

---

### Toolchain

![Solidity](https://img.shields.io/badge/Solidity-%23363636.svg?style=for-the-badge&logo=solidity&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white)
![Python](https://img.shields.io/badge/Python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![PHP](https://img.shields.io/badge/PHP-%23777BB4.svg?style=for-the-badge&logo=php&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-%23000000.svg?style=for-the-badge&logo=rust&logoColor=white)
![Vue.js](https://img.shields.io/badge/Vue.js-%2335495e.svg?style=for-the-badge&logo=vuedotjs&logoColor=%234FC08D)
![Docker](https://img.shields.io/badge/Docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![Postgres](https://img.shields.io/badge/Postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![Ethereum](https://img.shields.io/badge/Ethereum-3C3C3D?style=for-the-badge&logo=Ethereum&logoColor=white)

---

### Delivery spine — ERN out, DSR back

| Repository | What it does | Stack |
| :--- | :--- | :--- |
| [**stardust-distro**](https://github.com/zenith-repo/stardust-distro) | Music distribution platform — release ingest, DDEX delivery to DSPs | Vue · JavaScript |
| [**stardust-dsp**](https://github.com/zenith-repo/stardust-dsp) | The DSP side — receiving end of the delivery pipeline | Vue · JavaScript |
| [**ddex-suite**](https://github.com/zenith-repo/ddex-suite) | High-performance DDEX XML builder/parser with native bindings | Rust · JS |
| [**dedex**](https://github.com/zenith-repo/dedex) | Generic, efficient DDEX ERN parser | PHP |
| [**ddex-php**](https://github.com/zenith-repo/ddex-php) | PHP bindings for DDEX message handling | PHP |
| [**ddex-processor**](https://github.com/zenith-repo/ddex-processor) | DDEX XML ingest service | TypeScript |
| [**ddex-workbench**](https://github.com/zenith-repo/ddex-workbench) | Validation platform with web UI and API — ERN/DSR conformance | Vue · Python |
| [**dsrf**](https://github.com/zenith-repo/dsrf) | DDEX DSR parsing — the statement format royalties are actually paid from | Python |
| [**rd-portal-backend**](https://github.com/zenith-repo/rd-portal-backend) | Royalty statement ingestion, client roster, writer/publisher splits | Python |

### Contract layer — splits, standards, liquidity

| Repository | What it does | Stack |
| :--- | :--- | :--- |
| [**splits-contracts**](https://github.com/zenith-repo/splits-contracts) | Core 0xSplits contracts — deterministic revenue splits | Solidity · TypeScript |
| [**openzeppelin-contracts**](https://github.com/zenith-repo/openzeppelin-contracts) | The contract library everything else is built on | Solidity |
| [**ERC-3643**](https://github.com/zenith-repo/ERC-3643) | Permissioned security token — transfer-restricted by design | Solidity |
| [**zora-protocol**](https://github.com/zenith-repo/zora-protocol) | Creator coins and protocol SDKs | TypeScript · Solidity |
| [**v4-core**](https://github.com/zenith-repo/v4-core) | Uniswap v4 core — the AMM layer | Solidity |

### Data surface

| Repository | What it does | Stack |
| :--- | :--- | :--- |
| [**labelgrid-mcp**](https://github.com/zenith-repo/labelgrid-mcp) | Catalogue and royalty data API, exposed over MCP | TypeScript |

---

### Stats

<p>
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=zenith-repo&show_icons=true&theme=onedark&hide_border=true&include_all_commits=true&count_private=true" alt="stats" />
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=zenith-repo&theme=onedark&hide_border=true&layout=compact&langs_count=8" alt="top languages" />
</p>

---

<p align="center">
  <sub>DDEX ERN · DSR statements · ERC-3643 · epoch settlement · Merkle roots</sub><br/>
  <sub>Issues and discussion welcome on any repository above.</sub>
</p>
