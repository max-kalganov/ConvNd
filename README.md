# N-dimensional convolutional layer

## Description
This project aim is to experiment with N-dimensional convolution layers 
applied to regular features (*not visual features*). 

### Intuition
Convolution layer works on 2d data because it's able to extract 
positional data and use it for patterns recognition. Intuition for
this experiment is to test if there are any patterns in data 
positioning even if it's not a *Computer Vision* field, but regular 
data features.

### Experiment details
- Experiment is based on using tensorflow Conv layer, but for 
**N dimensions**
- Input data is normalized into ***0..1*** range
- Quantisation step is manually configured
- ***'Color'*** of a point in N-dimensional space is average class for
    that particular point  *(regarding quantisation)*
- ***'Color'*** is in range (0, 1]. 0 - means an empty cell
