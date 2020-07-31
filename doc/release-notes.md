0.21.1 Release Notes
improvements, as well as updated translations.

Please report bugs using the issue tracker at GitHub:

  <https://github.com/bitcoin/bitcoin/issues>

To receive security and update notifications, please subscribe to:

  <https://bitcoincore.org/en/list/announcements/join/>

How to Upgrade
==============

If you are running an older version, shut it down. Wait until it has completely
shut down (which might take a few minutes in some cases), then run the
installer (on Windows) or just copy over `/Applications/Bitcoin-Qt` (on Mac)
or `bitcoind`/`bitcoin-qt` (on Linux).

Upgrading directly from a version of Bitcoin Core that has reached its EOL is
possible, but it might take some time if the data directory needs to be migrated. Old
wallet versions of Bitcoin Core are generally supported.

Compatibility
==============

Bitcoin Core is supported and extensively tested on operating systems
using the Linux kernel, macOS 10.12+, and Windows 7 and newer.  Bitcoin
Core should also work on most other Unix-like systems but is not as
frequently tested on them.  It is not recommended to use Bitcoin Core on
unsupported systems.

From Bitcoin Core 0.20.0 onwards, macOS versions earlier than 10.12 are no
longer supported. Additionally, Bitcoin Core does not yet change appearance
when macOS "dark mode" is activated.

Notable changes

### Mining
- #19019 Fix GBT: Restore "!segwit" and "csv" to "rules" key (luke-jr)

### P2P protocol and network code
- #19219 Replace automatic bans with discouragement filter (sipa)

### Wallet
- #19300 Handle concurrent wallet loading (promag)
- #18982 Minimal fix to restore conflicted transaction notifications (ryanofsky)

### RPC and other APIs
- #19524 Increment input value sum only once per UTXO in decodepsbt (fanquake)
- #19517 psbt: Increment input value sum only once per UTXO in decodepsbt (achow101)
- #19215 psbt: Include and allow both non_witness_utxo and witness_utxo for segwit inputs (achow101)

### GUI
- #19097 Add missing QPainterPath include (achow101)
- #19059 update Qt base translations for macOS release (fanquake)

### Build system
- #19152 improve build OS configure output (skmcontrib)
- #19536 qt, build: Fix QFileDialog for static builds (hebasto)

### Tests and QA
- #19444 Remove cached directories and associated script blocks from appveyor config (sipsorcery)
- #18640 appveyor: Remove clcache (MarcoFalke)

### Miscellaneous
- #19194 util: Don't reference errno when pthread fails (miztake)
- #18700 Fix locking on WSL using flock instead of fcntl (meshcollider)

Credits
=======

Thanks to everyone who directly contributed to this release:

- Aaron Clauson
- Andrew Chow
- fanquake
- Hennadii Stepanov
- João Barbosa
- Luke Dashjr
- MarcoFalke
- MIZUTA Takeshi
- Pieter Wuille
- Russell Yanofsky
- sachinkm77
- Samuel Dobson
- Wladimir J. van der Laan

As well as to everyone that helped with translations on
[Transifex](https://www.transifex.com/bitcoin/bitcoin/).
