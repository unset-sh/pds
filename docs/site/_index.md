---
title: "PDS"
description: "Packaging and customisation of the unset.sh AT Protocol Personal Data Server."
type: docs
cascade:
  type: docs
menus:
  main:
    weight: 130
params:
  doc_kind: overview
---

`unset-sh/pds` holds the packaging and customisation of the AT Protocol Personal Data Server that unset.sh runs,
and builds its image.

**Status: repository foundation only.** No runnable PDS package or deployment configuration exists here yet.

## Boundaries

- Product integration with the PDS, including its privileged administration process, belongs in
  [backend](https://github.com/unset-sh/backend).
- Environment provisioning, storage, networking and secret references belong in
  [deployment](https://github.com/unset-sh/deployment), which runs the released PDS image.
- The upstream PDS keeps its own licence.

The [repository README](https://github.com/unset-sh/pds#readme) has the current notes. This section is exported
from `docs/site/` in `unset-sh/pds`; edit it there.
