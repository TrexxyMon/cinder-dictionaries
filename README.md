# Cinder Dictionaries

Optional offline dictionary data for [Cinder Reader](https://cinderreader.com).
This repository distributes dictionary data, manifests and attribution notices.
It does not contain the Cinder application source code.

## English — WordNet 3.1

[Download the English pack](https://github.com/TrexxyMon/cinder-dictionaries/releases/download/en-wordnet-3.1-v1/en-wordnet-3.1-v1.sqlite)

| Property | Value |
| --- | --- |
| Pack ID | `en-wordnet` |
| Pack version | `3.1-v1` |
| Headword and definition language | English |
| Indexed headwords | 147,478 |
| Definition groups | 117,791 |
| Size | 26,976,256 bytes (25.7 MiB) |
| Format | SQLite, `cinder-dictionary-1` |

The pack contains definitions, examples, synonyms and irregular-word mappings
from WordNet. Coverage differs from Cinder's online dictionaries. Audio and
pronunciations are not included.

In a Cinder version with offline dictionary support, open **Settings → Dictionary
→ Built-in → Offline Dictionaries**, download English and enable **Use Offline
Dictionaries**. You can turn off **Search Online If Not Found** to keep built-in
lookups offline. Alternatively, use **Import Dictionary Pack** with this release's
SQLite file. Older Cinder versions do not support these packs.

Dictionary packs are optional, stored on the device and removable. They are not
book files or executable extensions. The application verifies each approved pack
before activation.

## Source and attribution

WordNet 3.1 Copyright 2011 by Princeton University. All rights reserved.

- [WordNet project](https://wordnet.princeton.edu/)
- [Official database downloads](https://wordnet.princeton.edu/download/current-version)
- Source archive: `https://wordnetcode.princeton.edu/wn3.1.dict.tar.gz`
- [Complete WordNet license and disclaimer](LICENSE-WordNet.txt)

The data has been reorganized into an indexed SQLite database for offline lookup.
The complete copyright, license and disclaimer are embedded in the database's
metadata and supplied alongside every release. Retain these notices when copying
or redistributing the data. No endorsement by Princeton University is implied.

## Integrity and revisions

[manifest.json](manifest.json) records the exact file size, MD5 and SHA-256.
MD5 is used for native download-corruption checks, not as a security signature.
Use SHA-256 to independently verify the release file:

```powershell
Get-FileHash ./en-wordnet-3.1-v1.sqlite -Algorithm SHA256
```

Expected SHA-256:

```text
254b18bc659ae373ea6b54fe25fe76d8f842625c3ec51b69c9b973d2ee8ba04c
```

Published pack revisions must not be overwritten. Corrections use a new version
and a new release asset so existing installations can verify their original pack.
Additional languages require separately reviewed data and source licenses.
