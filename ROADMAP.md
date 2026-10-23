<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
FLIGHT-RECORDER — repository governance and provenance
-->

# Roadmap

Implemented local tooling validates repository metadata, maintained source and licences, workflows, development dependencies, documentation and inventory through fixed commands. It does not capture or reconstruct device events.

The planned Python library and simulation model require an earlier complete capture contract: actual event classes and payload layouts, unit/package identity, clocks and uncertainty, event and segment sequences, target widths, reset epochs, ring capacity, total byte budgets and provider protocol. Wire integers do not select a hardware width or board.

Future bounded capture preserves logical sequence independently of physical ring slots. Payload, metadata, alignment, checkpoints, staging, trigger journals and pending buffers count under their declared budgets. A ring cannot overwrite the only surviving anchor while claiming earlier history is known.

Segments will carry canonical unpadded base64url payloads and hashes of decoded raw bytes. Required predecessor identity remains required when bytes are unavailable. Protected or offloaded checkpoints must actually survive; a later checkpoint is a separate reconstruction input and cannot rewrite old sealed content or create a self-reference.

Periodic, on-demand and freeze-on-event are distinct trigger behaviors with declared windows, priority, coalescing and offload policy. Recording freeze does not actuate the model or device. Missing post-event data stays unavailable.

The intended public operations are verify, offload, reconstruct and export. They are not installed here. Reconstruction preserves duplicate/conflict quarantine, proven gaps, unknown prefixes, separate epochs and capture limits without interpolation. Sharing policy controls raw export; Field Ops receives a separate compact lane.

Completion requires all owned fields and original cases, independent references, real public producers and separate consumers, the complete simulation and SystemVerilog counterpart, supported target acceptance, strict native checks, meaningful coverage, documentation and fresh comparison benchmarks. Simulation does not qualify physical instrumentation or complete recorded history. Hosted services, device qualification and legal compliance are not asserted.
