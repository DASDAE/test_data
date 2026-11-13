# test_data
A repo of *small* files useful for testing DASDAE codes

## Data sources and attribution

Unless noted otherwise, files were contributed directly by DASDAE developers or instrument vendors.

The following files are trimmed (but otherwise unmodified) excerpts from the Global DAS Month February 2023 contributions hosted on [PubDAS](https://doi.org/10.1785/0220220279), licensed [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) (see each contribution's ReadMe on PubDAS for details):

- `das/optasense_odh4_1.h5` — University of Wisconsin-Madison, SURF (Sanford Underground Research Facility) array, OptaSense ODH-4 layout.
- `das/silixa_h5_ingv_1.h5` — INGV Osservatorio Etneo, Mt. Etna array, Silixa iDAS (Carina) netCDF-flavored layout.

Additional external sources:

- `das/ai4eps_1.h5` — trimmed excerpt of event `ci37280444` (Ridgecrest north array) from the [AI4EPS quakeflow_das dataset](https://huggingface.co/datasets/AI4EPS/quakeflow_das) (MIT license).
- `das/silixa_h5_idas2_1.h5` — the older Silixa iDAS (software 2.4) HDF5 layout, a `raw_das_data` dataset with snake_case string attrs, from member `Data_Custom_Model4/idas2_UTC_20200715_142650.719_rhone1khz.hdf5` of `Data_Custom_Model4.zip` in Willis, Walter, Fichtner and Martin, *Rhonegletscher DAS Cryoseismic Training Dataset, Features, and Comprehensive Catalog* ([doi:10.5281/zenodo.17555409](https://doi.org/10.5281/zenodo.17555409), CC BY 4.0). Trimmed to the first 400 samples × 40 channels with all attrs kept; the extent attrs (`samples`, `channels`, `endtime`, `stop_distance_m`, `measure_length_m`) are rewritten to match the trimmed array. Data values are unmodified.
- `das/nokia_ofdr_1` and `das/nokia_ofdr_downsampled_1.h5` — the Nokia Bell Labs multi-span (OFDR) binary layout and its manually downsampled HDF5 variant, from the OOI Regional Cabled Array 2025–2026 experiment ([doi:10.5281/zenodo.19930402](https://doi.org/10.5281/zenodo.19930402), CC BY 4.0). Headers and acquisition metadata come from real files, with host details removed and the file cut to 10 chunks (binary) or a 500 × 256 slab (HDF5). The array values are seeded synthetic noise, not recorded data.
- `das/opto_das_v7_1.hdf5` — OptoDAS file version 7 layout, member `data/ntp_sync/021040.hdf5` of [doi:10.5281/zenodo.11212055](https://doi.org/10.5281/zenodo.11212055) (CC BY 4.0). Cut to the first 10 samples × 20 channels of the recorded data; the per-channel and extent fields (`header/channels`, `nSamples`, `nChannels`, `phiOffs`, `cableSpec/sensorDistances`, `demodSpec/roiEnd` and the processing-chain channel `roi`) are shortened to match. All other metadata, values and dtypes are unchanged.
- `dts/kolsass_dts_netcdf3.nc` — netCDF-3 classic CF file, member `InnDEX22_distributed_temperature_sensing_20220608.nc` of `InnDEX22_distributed_temperature_sensing.zip` in [doi:10.5281/zenodo.10522708](https://doi.org/10.5281/zenodo.10522708) (CC BY 4.0). Cut to 200 times (indices 45302–45501, the first recorded samples; earlier ones are fill values) × the first 40 depths and written back as netCDF-3 classic; global and variable attributes, names and dtypes are unchanged.

