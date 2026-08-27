# Wanxiang Gram Snapshots

An archival mirror of the rolling Wanxiang LTS grammar model from [amzxyz/RIME-LMDG](https://github.com/amzxyz/RIME-LMDG).

This repository periodically snapshots the upstream `wanxiang-lts-zh-hans.gram` model into immutable, versioned GitHub Releases.

## Why?

The upstream LTS model is published at a stable URL:

```text
https://github.com/amzxyz/RIME-LMDG/releases/download/LTS/wanxiang-lts-zh-hans.gram
```

However, the contents of this asset are updated in place over time.

This makes it unsuitable for package managers and reproducible system configurations that require an artifact to remain available at a stable version with a stable checksum.

This repository solves that problem by periodically archiving the current upstream model as a versioned GitHub Release.

## Snapshots

GitHub Actions checks the upstream LTS model daily.

When a new upstream model is detected, an unmodified copy is published as a new Release.

Release tags use the upstream model asset's update time in GMT+8, formatted as:

```text
YYYYMMDDHHmmss
```

For example:

```text
20260823195706
```

corresponds to:

```text
2026-08-23 19:57:06 GMT+8
```

Each Release contains:

```text
wanxiang-lts-zh-hans.gram
```

together with provenance information and its SHA-256 digest in the Release notes.

If the upstream model has not changed, no new snapshot is created.

## Usage

A snapshot can be downloaded using its immutable Release URL:

```text
https://github.com/OrdChaos/RIME-LMDG.snapshot/releases/download/<snapshot>/wanxiang-lts-zh-hans.gram
```

For example:

```text
https://github.com/OrdChaos/RIME-LMDG.snapshot/releases/download/20260823195706/wanxiang-lts-zh-hans.gram
```

Consumers should pin both the snapshot tag and the expected cryptographic hash.

## Upstream

The model originates from:

**RIME-LMDG**
https://github.com/amzxyz/RIME-LMDG

Upstream rolling release:

https://github.com/amzxyz/RIME-LMDG/releases/tag/LTS

This repository is an independent archival mirror. It is not affiliated with or endorsed by the RIME-LMDG project or its maintainers.

The archived model files are copied without modification.

## License

The Wanxiang grammar model is distributed by its upstream authors under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** license.

See:

https://creativecommons.org/licenses/by/4.0/

The model snapshots in this repository remain subject to the upstream CC BY 4.0 license.

Attribution belongs to the original RIME-LMDG project and its contributors. This repository does not claim authorship of, or relicense, the archived model.

CC BY 4.0 permits sharing and redistribution of the material, including for commercial purposes, provided that appropriate attribution is given and the applicable license requirements are followed.

Any scripts, GitHub Actions workflows, or other original code in this repository are separately licensed as indicated by this repository.

## Integrity

Snapshots are intended to preserve a specific historical upstream artifact.

Consumers should verify the SHA-256 digest recorded with each Release rather than relying solely on the filename or Release URL.

Snapshot files are not modified, recompressed, or otherwise transformed before publication.

## Disclaimer

This repository is provided as an archival service for reproducibility and historical availability.

No warranty is provided regarding the correctness, fitness, availability, or continued upstream support of any archived model.
