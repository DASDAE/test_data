# test_data
A repo of *small* files useful for testing DASDAE codes

## Data sources and attribution

Unless noted otherwise, files were contributed directly by DASDAE developers or instrument vendors.

The following files are trimmed (but otherwise unmodified) excerpts from the Global DAS Month February 2023 contributions hosted on [PubDAS](https://doi.org/10.1785/0220220279), licensed [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) (see each contribution's ReadMe on PubDAS for details):

- `das/optasense_odh4_1.h5` — University of Wisconsin-Madison, SURF (Sanford Underground Research Facility) array, OptaSense ODH-4 layout.
- `das/silixa_h5_ingv_1.h5` — INGV Osservatorio Etneo, Mt. Etna array, Silixa iDAS (Carina) netCDF-flavored layout.

Additional external sources:

- `das/ai4eps_1.h5` — trimmed excerpt of event `ci37280444` (Ridgecrest north array) from the [AI4EPS quakeflow_das dataset](https://huggingface.co/datasets/AI4EPS/quakeflow_das) (MIT license).
- `das/nokia_ofdr_1` and `das/nokia_ofdr_downsampled_1.h5` — the Nokia Bell Labs multi-span (OFDR) binary layout and its manually downsampled HDF5 variant, from the OOI Regional Cabled Array 2025–2026 experiment ([doi:10.5281/zenodo.19930402](https://doi.org/10.5281/zenodo.19930402), CC BY 4.0). Headers and acquisition metadata come from real files, with host details removed and the file cut to 10 chunks (binary) or a 500 × 256 slab (HDF5). The array values are seeded synthetic noise, not recorded data.
- `das/opto_das_v7_1.hdf5` — OptoDAS file version 7 layout, member `data/ntp_sync/021040.hdf5` of [doi:10.5281/zenodo.11212055](https://doi.org/10.5281/zenodo.11212055) (CC BY 4.0). Cut to the first 10 samples × 20 channels of the recorded data; the per-channel and extent fields (`header/channels`, `nSamples`, `nChannels`, `phiOffs`, `cableSpec/sensorDistances`, `demodSpec/roiEnd` and the processing-chain channel `roi`) are shortened to match. All other metadata, values and dtypes are unchanged.
