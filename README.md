# DLInfer_dataset
A dataset built for the DLIner. The hierarchy of the DLInfer and data are shown as follows:
---

>data. Extracted variable information, including slice, variable name, location and type.
>>data_dynamic. Data using in RQ2 test, RQ3 training and test stores in this folder.
>>>dynamic_json. Dynamic dataset using in RQ2, RQ3 test by running the testcases in 10 repos.
>>>data_static. Static dataset using in RQ1, RQ2 is extracted by pysonar2 and pyslicer.
>>>>train. Static dataset using in RQ1, RQ2 training.
>>>>valid. Static dataset using in RQ1, RQ2 validation.
>>>>test. Static dataset using in RQ1 test.

>DLInfer_data. Original repos using in the RQs. These repos will be extracted in data preparation.
>>star_orig_pro_train. Select 560 Github repos to build the training dataset. The source code of these 560 repos are in this folder.
>>star_pro_pysonar_train. Infer static type information of these 560 repos using pysonar2.
>>star_orig_pro_valid. Select 70 Github repos to build the validation dataset. The source code of these 70 repos are in this folder.
>>star_pro_pysonar_valid. Infer static type information of these 70 repos using pysonar2.
>>star_orig_pro_test. Select 70 Github repos to build the test dataset. The source code of these 70 repos are in this folder.
>>star_pro_pysonar_test. Infer static type information of these 70 repos using pysonar2.
>>orig_pro_dynamic. Select 10 Github repos to evaluate RQ2, RQ3. The source code of these 10 repos are in this folder.
>>pro_pysonar_dynamic. Infer static type information of these 10 repos using pysonar2.

> DLInfer-master. The implementation of prototype tool.
>>DLInfer. All the drivers are in this folder.
>>data_static. Dataset is used in the RQ1.
>>data_dynamic. Dataset is used in the RQ2 and RQ3.
>>rq1. Dataset is used to evaluate RQ1 and is built by the DLInfer drivers.
>>rq2. Dataset is used to evaluate RQ2 and is built by the DLInfer drivers.
>>rq3. Dataset is used to evaluate RQ3 and is built by the DLInfer drivers.
---
## Step1. Data preparation
Unzip the *.zip in the data_dynamic and data_static. 

## Build source code repos if needed.
If you want to extract the dataset from source code. Move the DLInfer_data to the parent folder. DLInfer will be in the same folder with data. We already extract variables' information in the data, DLInfer-master/data_static and DLInfer-master/data_dynamic.
## Step2. Evaluation.
Move data and DLInfer_data in the same folder with DLInfer-master. Then run the scripts according to the DLInfer-master's document.

