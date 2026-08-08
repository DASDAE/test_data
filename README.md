# test_data
A repo of *small* files useful for testing DASDAE codes

## Data sources and attribution

Unless noted otherwise, files were contributed directly by DASDAE developers or instrument vendors.

The following files are trimmed (but otherwise unmodified) excerpts from the Global DAS Month February 2023 contributions hosted on [PubDAS](https://doi.org/10.1785/0220220279), licensed [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) (see each contribution's ReadMe on PubDAS for details):

- `das/optasense_odh4_1.h5` — University of Wisconsin-Madison, SURF (Sanford Underground Research Facility) array, OptaSense ODH-4 layout.
- `das/hdas_1.h5` — Instituto Geográfico Nacional (Spain), ADIF train-track array, Aragón Photonics HDAS layout (`File_Header` variant).
- `das/hdas_2.h5` — ICM-CSIC, Canalink submarine cable (Tenerife), Aragón Photonics HDAS layout (`hdas_header` variant).
- `das/silixa_h5_ingv_1.h5` — INGV Osservatorio Etneo, Mt. Etna array, Silixa iDAS (Carina) netCDF-flavored layout.

Additional external sources:

- `das/ai4eps_1.h5` — trimmed excerpt of event `ci37280444` (Ridgecrest north array) from the [AI4EPS quakeflow_das dataset](https://huggingface.co/datasets/AI4EPS/quakeflow_das) (MIT license).
