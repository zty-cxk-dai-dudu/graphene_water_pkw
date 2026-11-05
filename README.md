# Graphene-supported water: provenance and selected source tables

This private repository is being assembled for the graphene-layer-dependent water proton-sharing and ionization study. It is a versioned record of source data, not yet a complete public reproducibility release.

## Included data

`source_data/` contains four numerical CSV files copied without modification from the archived zty package `JACS_code_data_20260914_v23/graphene_water_code_data/source_data/derived/`:

- `f3_sharing_populations_v17.csv`: proton-sharing population summary.
- `f4_all_site_display_v17.csv`: site-resolved pKw display values.
- `f4_basin_means.csv`: free-energy basin means.
- `f4_acceptor_contrasts.csv`: acceptor contrast values.

These are **archived v23 results**. That package describes classical C1/C2 windows of 600–1000 ps and C4 and quantum windows of 100–500 ps. Later manuscript edits state 600–1000 ps for all conditions. The CSVs have not been recalculated for those later window choices and must not be described as current-window results.

## JACS reference and scope

Dasgupta, Saha and Paesani, JACS 2025, DOI: 10.1021/jacs.5c08273, released a frozen potential and the complete DeePMD training and validation sets at [their data repository](https://github.com/paesanilab/Data_Repository/tree/main/DC-r2SCAN_water_autoionization_nanoconfinement). Their release is the target organization for a future complete release here.

The model paths and dataset inventory in `MODEL_DATA_INVENTORY.md` refer to multiple historical zty training campaigns. The final models used for the revised manuscript still require an exact model-to-calculation mapping before frozen weights or training/validation arrays can be published as the definitive set. In particular, the inspected 1L 200k model uses a BLYP-D3 reference, while the inspected 2L 300k and 4L 500k models use PBE-D3(BJ); these cannot be represented as a single uniform DFT training set.

The repository remains private while provenance, final model identity, and data-window consistency are resolved.
