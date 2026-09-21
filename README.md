# SetupMeld Docking Station Compatibility Matrix data

Machine-readable data for the [SetupMeld Docking Station Compatibility Matrix](https://setupmeld.com/guides/docking-station-laptop-compatibility/). The SetupMeld page is the canonical citation target; this directory or its public repository is only a distribution carrier.

## Release

- Schema version: 1.1.0
- Data version: 2026-09-16.5
- License: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) — reuse is allowed with attribution.

## Files

- `matrix-facts.json`: canonical, fact-level source. This is the only hand-maintained data file.
- `matrix-facts.csv`: generated fact-level view, one record per Matrix cell or historical version.
- `matrix-wide.json`: generated one-model-per-row view.
- `matrix-wide.csv`: generated one-model-per-row view.

## Field and evidence rules

The fixed field vocabulary is: `host_support`, `display_capability`, `display_interfaces`, `switching_method`, `keyboard_mouse_channel`, `peripheral_usb_capability`, `clamshell_support`, `power_delivery`, `known_non_working_combinations`, `official_support_evidence`, `public_user_report`.

Every active record has exactly one `source_type`: `official_specification`, `official_support`, or `public_user_report`. Verification is a separate `status`: `verified`, `pending`, or `not_applicable`. Historical closed v1.0 rows retain their original vocabulary for auditability.

Public-user-report summaries also preserve `evidence_strength`, `independent_report_count`, and `conflict_variables`. PARTIAL reports do not enter the Evidence Layer and do not count toward independent_report_count.

`source_scope=model_source_set` means the published page supplied a set of official sources for the model but did not assign one URL to one capability cell. Do not represent that as cell-level attribution. Provenance refinement is append-only: close the old record with `valid_to` and append a new record with higher precision.

## Citation

SetupMeld, Docking Station Compatibility Matrix, data version {data_version}, https://setupmeld.com/guides/docking-station-laptop-compatibility/, cell source: {source_urls}.

Replace `{data_version}` with this release's data version and `{source_urls}` with the cited record's source URL or source set. Cite the SetupMeld Matrix page, not the repository.
