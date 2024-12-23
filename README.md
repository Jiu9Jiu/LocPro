## LocPro

## Installation

```bash
git clone https://github.com/idrblab/LocPro.git
cd LocPro
conda env create -f environment.yml
conda activate LocPro

# download models from https://drive.google.com/drive/folders/1twlsmrQRBF7gFMG97tnH0HxzjvExyfsA
# and extract them to ./models
```


## Run LocPro

```python
from locpro.inference import getInference
import pandas as pd
from fasta import FASTA


output_folder = 'result_demo'
input_fasta_path = "./demo.fasta"
input_fasta = FASTA(input_fasta_path)

# Perform inference using the "Main" model type
result_main,result_all = getInference(input_fasta=input_fasta, output_folder=output_folder)
pd.DataFrame(result_main).to_csv(f'./{output_folder}/resultMain.csv', index=False)

```
