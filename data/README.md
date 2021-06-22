# Data preparation

The project uses the data from a challenge on Second Language Acquisition Modeling<sup>1</sup> organised by Duolingo AI in conjunction with the 13th BEA Workshop and NAACL-HLT 2018 conference. The challenge disription is availalbe on its [official web page](http://sharedtask.duolingo.com/2018). This project is aimed to explore if any available or synthesised feature can be used to predict potential errors.

The data is analysed using R. To preprocess the original data<sup>2</sup> for replication purposes,
use the following instructions.

1. Download the `dataverse_files.zip` archive from [Harvard Dataverse](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/8SWHNO) and put in this folder, i.e. `./data`.

2. Run the following `bash` command to create necessary folders, preprocess files and remove anything that is not used for this project.

```bash
    ./preprocess_data
```

3. It is possible to skip the first two steps if you wish to reproduce only experiments with glmer models. For this, only files `df.csv`, `sample_df.csv` and `trigrams.csv` are necessary.

NB: Check if `codebase/awk_metadata`, `codebase/awk_sessions` and `preprocess_data` files are executable. If not, run `chmod +x <fileName>` and re-run Step 2

Only `train` split is being analysed using the Null Hypothesis Significance Testing framework, `dev` and `test` are removed.

References

1. B. Settles, C. Brust, E. Gustafson, M. Hagiwara, and N. Madnani. 2018. Second Language Acquisition Modeling. In Proceedings of the NAACL-HLT Workshop on Innovative Use of NLP for Building Educational Applications (BEA). ACL.

2. Settles, Burr. 2018. “Data for the 2018 Duolingo Shared Task on Second Language Acquisition Modeling
(SLAM).” Harvard Dataverse. https://doi.org/10.7910/DVN/8SWHNO.
