# lwda-paper

Universal adversarial perturbations (UAPs) are small perturbations imposed on images that are able to fool a single convolutional neural network image classifier. They have been shown to generalise well to other neural networks. Here, we report on our reproduction effort of the results given in a work by Moosavi-Dezfooli et al. on UAPs and study two methods to construct UAPs for several neural networks. While the results are not strong enough to make general conclusions, they suggest that UAPs indeed profit from being constructed on several neural networks. Also, we show that a linear interpolation between two UAPs does not produce a viable UAP on both networks.

## Results

The following table shows the achieved fooling rates on different models.
The columns indicate the network used to generate the UAP, while the rows give the network on which the fooling rate is measured. The main diagonal therefore contains the self-fooling rates, i.e. the fooling rates achieved using the same model for generating the perturbation and measuring the fooling rate. 

|                   | VGG-F | Inception | VGG-16 | VGG-19 | ResNet-152 |
|-------------------|-----|-----|-----|-----|----|
| **VGG-F**         | 90% | 56% | 32% | 32% | 24% |
| **Inception**     | 42% | 82% | 16% | 16% | 16% |
| **VGG-16**        | 46% | 60% | 59% | 52% | 38% |
| **VGG-19**        | 45% | 58% | 51% | 54% | 33% |
| **ResNet-152**    | 42% | 55% | 31% | 33% | 73% |
