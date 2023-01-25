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

### Algorithm approaches
1. Train model to recover class for masked data points
</br>On eval - mask test samples and predict classes for them.

2. Train model as autoencoder (replace ***number of points*** in a cell with ***class*** in the decoder output). 
Pass input data as an additional input head at the later stages of
the encoder to get a single output class for the input data point.

### Test cases

1. Simple case
   - several data centroids
   - same number of data for each centroid
   - clearly separated clusters
2. Mid-level case
   - several data centroids
   - different size of clusters
   - overlapping clusters
3. Special case 1
   - Data on a straight line - one cluster, otherwise - another
4. Special case 2
   - Data in and out of a circle
5. Special case 3
   - Single class data in the center
