<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
FLIGHT-RECORDER — repository governance and provenance
-->

# Validation tooling API

The metadata command accepts `--root` and `--json`. The inventory command additionally accepts `--mode generate|verify` and requires `--output` only for generation. All commands emit safe structured JSON. Exits are 0 for the requested scope, 2 for refusal, 3 for unavailable required inputs or tools, and 4 for invalid invocation or configuration.

Metadata validation accepts no generated inventory dependency. Inventory generation publishes deterministic new bytes; verification requires the canonical inventory and complete initial paths. A successful operation does not qualify capture, surviving anchors or reconstructed history or establish release readiness.

## Metadata acceptance

::: recorder_validation.metadata.validate_metadata

## Finite input

::: recorder_validation.inputs.read_file

::: recorder_validation.inputs.read_json

## Capability inventory

::: recorder_validation.capabilities.inventory_bytes

::: recorder_validation.capabilities.create_inventory

::: recorder_validation.capabilities.validate_capabilities

## Diagnostics

::: recorder_validation.report.Finding

::: recorder_validation.report.Report

## Command interfaces

::: recorder_validation.cli.metadata_main

::: recorder_validation.cli.inventory_main

## Source ownership and maintained tree

::: recorder_validation.provenance.validate_notice

::: recorder_validation.provenance.validate_provenance

::: recorder_validation.structure.maintained_paths

::: recorder_validation.structure.validate_structure

## YAML and workflow policy

::: recorder_validation.yaml_input.read_yaml

::: recorder_validation.workflows.validate_workflows

## Complete dependency observations

Release candidates and observed installed metadata are separate records. The hash lock covers the entire selected development graph. Exact source-builder constraints also use that lock. Recorded installation RECORD hashes are observations; relocated entry-script paths prevent treating them as universal build identities. Custom licence references retain exact source terms and do not infer permissions.

::: recorder_validation.dependency_lock.parse_direct

::: recorder_validation.dependency_lock.parse_lock

::: recorder_validation.dependency_records.Artifact

::: recorder_validation.dependency_records.LicenseEvidence

::: recorder_validation.dependency_records.LicenseSource

::: recorder_validation.dependency_records.PackageRecord

::: recorder_validation.dependency_records.read_provenance

::: recorder_validation.dependencies.verify_records

::: recorder_validation.dependencies.verify_installed

::: recorder_validation.dependencies.verify_configuration

::: recorder_validation.dependencies.validate_dependencies

::: recorder_validation.native_tools.verify_native_tools

## Actual documentation rendering

::: recorder_validation.documentation.References

::: recorder_validation.documentation.render_markdown

::: recorder_validation.documentation.inspect_markdown

::: recorder_validation.documentation.build_site

::: recorder_validation.documentation.inspect_projection

::: recorder_validation.documentation.validate_documentation

## Tool completion and scoped preflight

Every tool uses a fixed absolute executable, literal arguments and a finite deadline. Actual exits survive communication errors where observed. Output limits apply to accepted completed output; the caller reserves process memory separately. A named preflight subset reports its narrower scope. The complete operation requires the entire compiled profile. Missing tools, invalid protocol and native failures retain their real states.

::: recorder_validation.execution.ToolResult

::: recorder_validation.execution.run_tool

::: recorder_validation.preflight.Check

::: recorder_validation.preflight.Outcome

::: recorder_validation.preflight.PreflightReport

::: recorder_validation.preflight.validate_checker_report

::: recorder_validation.preflight.run_check

::: recorder_validation.preflight.run_checks

::: recorder_validation.preflight.source_payload

::: recorder_validation.validation_profile.scaffold_checks

::: recorder_validation.preflight_cli.preflight_main

## Shared command and protocol interfaces

::: recorder_validation.inputs.parse_json

::: recorder_validation.report.Refusal

::: recorder_validation.cli.Parser

::: recorder_validation.cli.check_main

::: recorder_validation.cli.emit_report

::: recorder_validation.ci_dependencies.verify_ci_dependencies

## Native workflow composition

The coordinator executes the eight complete native jobs from the maintained workflow sources. Each of four category gates requires every actual descendant result, and the stable required gate checks all four category results. The workflow policy verifies exact job equality with each source and rejects missing descendants, masked outcomes, altered commands and workflow calls. This preserves all category checks without depending on an unsupported reusable-workflow syntax. Both native syntax and unchanged pedantic workflow checks inspect the actual executable configuration; no projected input or suppressed finding is used.
