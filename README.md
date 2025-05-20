# Predicts activity of compounds accross the Tox21 panel

Predicts activity of compounds in the Tox21 toxicity panel, comprising of 12 toxicity pathways, as part of the MoleculeNet benchmark datasets. This model has been trained using the GROVER transformer (see eos7w6n or grover-embedding for a detail of the molecular featurization step with GROVER)

This model was incorporated on 2022-07-12.

## Information
### Identifiers
- **Ersilia Identifier:** `eos5smc`
- **Slug:** `grover-tox21`

### Domain
- **Task:** `Annotation`
- **Subtask:** `Activity prediction`
- **Biomedical Area:** `ADMET`
- **Target Organism:** `Homo sapiens`
- **Tags:** `Tox21`, `Toxicity`, `Chemical graph model`

### Input
- **Input:** `Compound`
- **Input Dimension:** `1`

### Output
- **Output Dimension:** `12`
- **Output Consistency:** `Fixed`
- **Interpretation:** Toxicity measurements against 12 biological targets

Below are the **Output Columns** of the model:
| Name | Type | Direction | Description |
|------|------|-----------|-------------|
| nr_ar | float | high | Probability of inhibition of the Tox21 target nr_ar |
| nr_ar_lbd | float | high | Probability of inhibition of the Tox21 target nr_ar_lbd |
| nr_ahr | float | high | Probability of inhibition of the Tox21 target nr_ahr |
| nr_aromatase | float | high | Probability of inhibition of the Tox21 target nr_aromatase |
| nr_er | float | high | Probability of inhibition of the Tox21 target nr_er |
| nr_er_lbd | float | high | Probability of inhibition of the Tox21 target nr_er_lbd |
| nr_ppar_gamma | float | high | Probability of inhibition of the Tox21 target nr_ppar_gamma |
| sr_are | float | high | Probability of inhibition of the Tox21 target sr_are |
| sr_atad5 | float | high | Probability of inhibition of the Tox21 target sr_atad5 |
| sr_hse | float | high | Probability of inhibition of the Tox21 target sr_hse |

_10 of 12 columns are shown_
### Source and Deployment
- **Source:** `Local`
- **Source Type:** `External`
- **DockerHub**: [https://hub.docker.com/r/ersiliaos/eos5smc](https://hub.docker.com/r/ersiliaos/eos5smc)
- **Docker Architecture:** `AMD64`, `ARM64`
- **S3 Storage**: [https://ersilia-models-zipped.s3.eu-central-1.amazonaws.com/eos5smc.zip](https://ersilia-models-zipped.s3.eu-central-1.amazonaws.com/eos5smc.zip)

### Resource Consumption
- **Model Size (Mb):** `1310`
- **Environment Size (Mb):** `2408`
- **Image Size (Mb):** `6273.84`

**Computational Performance (seconds):**
- 10 inputs: `49.17`
- 100 inputs: `445.26`
- 10000 inputs: `-1`

### References
- **Source Code**: [https://github.com/tencent-ailab/grover](https://github.com/tencent-ailab/grover)
- **Publication**: [https://arxiv.org/abs/2007.02835](https://arxiv.org/abs/2007.02835)
- **Publication Type:** `Preprint`
- **Publication Year:** `2020`
- **Ersilia Contributor:** [Amna-28](https://github.com/Amna-28)

### License
This package is licensed under a [GPL-3.0](https://github.com/ersilia-os/ersilia/blob/master/LICENSE) license. The model contained within this package is licensed under a [MIT](LICENSE) license.

**Notice**: Ersilia grants access to models _as is_, directly from the original authors, please refer to the original code repository and/or publication if you use the model in your research.


## Use
To use this model locally, you need to have the [Ersilia CLI](https://github.com/ersilia-os/ersilia) installed.
The model can be **fetched** using the following command:
```bash
# fetch model from the Ersilia Model Hub
ersilia fetch eos5smc
```
Then, you can **serve**, **run** and **close** the model as follows:
```bash
# serve the model
ersilia serve eos5smc
# generate an example file
ersilia example -n 3 -f my_input.csv
# run the model
ersilia run -i my_input.csv -o my_output.csv
# close the model
ersilia close
```

## About Ersilia
The [Ersilia Open Source Initiative](https://ersilia.io) is a tech non-profit organization fueling sustainable research in the Global South.
Please [cite](https://github.com/ersilia-os/ersilia/blob/master/CITATION.cff) the Ersilia Model Hub if you've found this model to be useful. Always [let us know](https://github.com/ersilia-os/ersilia/issues) if you experience any issues while trying to run it.
If you want to contribute to our mission, consider [donating](https://www.ersilia.io/donate) to Ersilia!
