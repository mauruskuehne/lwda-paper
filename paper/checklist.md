The Machine Learning Reproducibility Checklist (v2.0, Apr.7 2020)
For all models and algorithms presented, check if you include: 
- [ ] A clear description of the mathematical setting, algorithm, and/or model. 
- [ ] A clear explanation of any assumptions. 
- [ ] An analysis of the complexity (time, space, sample size) of any algorithm. 

For any theoretical claim, check if you include: 
- [ ] A clear statement of the claim. 
- [ ] A complete proof of the claim. 

For all datasets used, check if you include: 
- [ ] The relevant statistics, such as number of examples. 

* We used the ImageNet dataset for all models and tests: http://www.image-net.org

- [x] The details of train / validation / test splits. 

* train set for generating perturbations: 10'000 randomly selected images from the ImageNet train set.
* validation set to measure fooling rates: entire ImageNet validation set (50'000 images). 

- [ ] An explanation of any data that were excluded, and all pre-processing step. 
* We didn't use the entire ImageNet train set due to resource constraints.
* The preprocessing steps are given in the code TODO

- [x] A link to a downloadable version of the dataset or simulation environment. 
* The source code is available in this repository: https://github.com/mauruskuehne/lwda-paper

- [x] ~~For new data collected, a complete description of the data collection process, such as instructions to annotators and methods for quality control. ~~

For all shared code related to this work, check if you include: 

- [ ] Specification of dependencies. 
- [x] Training code. 

* The code used to generate perturbations is available [(here)<https://github.com/mauruskuehne/lwda-paper/tree/master/paper>]

- [x] Evaluation code. 

* The code used to evaluate perturbations is available [(here)<https://github.com/mauruskuehne/lwda-paper/tree/master/paper>]

- [ ] Pre-trained model(s).

* To evaluate the fooling rates we used the following networks and weights:
    * [(VGG-16)<https://github.com/keras-team/keras-applications>]
    * [(VGG-19)<https://github.com/keras-team/keras-applications>]
    * [(ResNet-152)<https://github.com/keras-team/keras-applications>]
    * [(Inception V1)<https://storage.googleapis.com/download.tensorflow.org/models/inception5h.zip>]
    * [(VGG-F)<http://www.robots.ox.ac.uk/~vgg/research/deep_eval/>] These model weights were converted to be tensorflow compatible. The converted weights are available here TODO


- [ ] README file includes table of results accompanied by precise command to run to produce those results. 



For all reported experimental results, check if you include: 
- [ ] The range of hyper-parameters considered, method to select the best hyper-parameter configuration, and specification of all hyper-parameters used to generate results. 

* The used hyper-parameters are documented in the paper [(here)<https://github.com/mauruskuehne/lwda-paper/tree/master/paper>]

- [ ] The exact number of training and evaluation runs. 

* All perturbations were generated using 20 UAP iterations.
* All perturbations were evaluated only once, on the entire validation set.

- [ ] A clear definition of the specific measure or statistics used to report results. 
- [ ] A description of results with central tendency (e.g. mean) & variation (e.g. error bars). 
- [ ] The average runtime for each result, or estimated energy cost. 
- [ ] A description of the computing infrastructure used.
