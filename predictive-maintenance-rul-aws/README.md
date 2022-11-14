# Building a Predictive Maintenance Solution Using AWS AutoML and No-code Tools

## Project description

The major goal of this repository is to represent the minimal set of materials required for the above named project to run. The project is described in detail in [this blog-article](https://docs.google.com/document/d/1Kb7J-rtY8JYvjrYUP-gQ12DdZ37d9rrOwkrNlA2YN30/edit?usp=sharing)

The goal of the project has been to develop a starter kit for predictive maintenance, namely, for estimation of the remaining useful life (RUL). The goal and results are described in the following quotations from the above mentioned blog-article: 

> In this article, we’ll describe how  equipment operators can build a predictive maintenance solution using AutoML and No-Code tools provided by AWS. This type of  solution  delivers significant gains to modern, large-scale industrial systems and mission-critical applications where the costs associated with machine failure or unplanned downtime are often unbearably high


> We developed two workflows for our clients who are interested in predicting  RUL for various types of equipment (not engines). The workflows are supposed to be performed by non-experts in ML, Data Science, and programming. Both workflows cover the creation and deployment of a ML model, and routine exploitation of said model for predicting RUL based on new data. We achieved this by using Amazon AutoML services: *AWS Canvas* and *AWS Sagemaker Autopilot*. In addition, we also demonstrated the operation of both approaches using NASA Turbofan Jet Engine Data Set.

The starter kit, besides the text with detailed desription of the workflows, comprises two notebooks:

 [AutopilotMakeModel.ipynb](https://colab.research.google.com/drive/1tlvcrNKuc67rZsBm7knNnDv8A5HFERmq)

 [AutopilotPredictRUL.ipynb](https://colab.research.google.com/drive/17Xu8hbXRWYZ9td8-rfU2sApbPfBc97gk)

Both notebooks are referred to in the article. Their local copies are in the folder `./notebooks`.

The first notebook (`AutopilotMakeModel.ipynb`) automates model training and deployment. The second notebook (`AutopilotPredictRUL.ipynb`) automates the process of inference itself; i.e. making predictions of RUL on the basis of new data. Both notebooks are accompanied by detailed comments, and, as such, both are self-explanatory.



## Repository structure

The repository includes the following folders:

- `./notebooks` is the folder with a working copy of the two notebooks;
- `./data/input` is the folder with two input files used by the notebooks;
- `./reports` contains the files produced by the notebook, mainly graphical files with a copy of the graphical output.

## Requirements

The project could be run from any account on the AWS platform.  It does not require installation of additional packages. See also the section [How to setup and run project](#how-to-setup-and-run-project)

## How to setup and run project

These notebooks can be run form AWS *Sagemaker* notebooks. Therefore, the following steps would be re quired:

- Open the Amazon *SageMaker* console at `https://console.aws.amazon.com/sagemaker/`
- Create a notebook instance. Since we are going to use *Sagemaker* service, it is going to allocate resources for our jobs. Hence, it is enough to choose a medium machine, for instance, `ml.t2.medium`.
- Also, For IAM role, choose *Create a new role*, and then choose *Create role*. This IAM role automatically gets permissions to access any S3 bucket that has sagemaker in the name. It gets these permissions through the AmazonSageMakerFullAccess policy, which *SageMaker* attaches to the role.
- Once notebook instance is created, we can launch *JupyterLab* and upload our notebooks. For kernel, we can select `conda_python3`. This kernel includes default *Anaconda* installation and *Python3*.
- Make sure to upload the relevant train and test data to the relevant AWS S3 storage. Run the notebook cells
 
## License

```
Copyright 2022 Grid Dynamics International, Inc. All Rights Reserved

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```

## Authors

- Volodymyr Koliadin, `vkoliadin@griddynamics.com`
- Andriy Drebot, `adrebot@griddynamics.com`
- Ilya Katsov, `ikatsov@griddynamics.com`

