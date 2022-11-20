##[Criteria of selecting subjects for RQ2 and RQ3]
For inferring variable types that cannot be inferred statically, we download many real-world projects on GitHub and install dependencies to test cases for collecting variable types at runtime.

The criteria of the ten projects selected for RQ2 and RQ3 are critical. 
(1) We filter many projects that we cannot run the testcases within the projects. Some projects may need to connect to a server or generate some dataset using outdated tools that our system cannot install. 
(2) We drop these projects with fewer dynamic variables or low test coverage by inspecting the runtime frames. Some projects can only pass several testcases, or their test coverage is lower than 30%. We select projects with about 80% test coverage or higher. 
(3)We exclude some projects whose types are extracted by inspecting from the runtime but cannot be used as ground truth, such as ”function.” 

The goal of RQ2 and RQ3 is to evaluate the effectiveness of
DLInfer in inferring the type information for the variables that can only be obtained at runtime, we need to run these subjects and collect the type information. In the experiment, we employ the test suites provided by the developers in the source code package to drive them. Thus, we sample ten subject programs with an extensive test suite and high coverage to conduct this experiment. The information on the test suite and coverage of the ten subjects are as follows:

Table I. Statistics of the dataset collected type information through dynamic analysis

  | Project | Files | Locs | Vstatic | Vdynamic | Testcases | LineCoverage |
  |:-------:|:-----:|:----:|:-------:|:--------:|:---------:|:---:|
  |mtgjson | 57   |6912  | 737  | 20   | 12   | 52%|
  |wemake  | 405  |55841 | 2748 | 459  | 32756| 99%|
  |cerberus| 176  |7324  | 570  | 18   | 395  | 95%|
  |bokeh   | 3702 |131931| 11895| 372  | 10440| 86%|
  |zfsp    | 54   |3554  | 600  | 214  | 54   | 87%|
  |invoke  | 284  |26159 | 1831 | 89   | 984  | 94%|
  |pygal   | 286  |13780 | 1169 | 176  | 4414 | 89%|
  |ansible | 5054 |285515| 20464| 302  | 3518 | 55%|
  |anaconda| 500  |90207 | 6719 | 189  | 784  | 58%|
  |sc2     | 131  |11205 | 480  | 3791 | 6    | 72%|
  |total   | 10649|632428| 39422| 5630 | 53363| 79%|



##[Working Directory]

(1) the "DLInfer" folder consists of the drivers.

(2) the "data_static" folder consists of the data for RQ 1, and the "data_dynamic" folder consists of the data for RQ 2 and RQ 3.

(3) the "rq1", "rq2" and "rq3" folders consist of the process and result data of corresponding experiments.

(4) the dynamic dataset consists of data_dynamic, static_txt and static_json, so unzip the corresponding zip files.
###This folder is the dynamic datset.
