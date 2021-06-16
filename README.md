# SSL-HETDEX
Here we apply a few SSL methods to the HETDEX data. 

We are currently interested in continuum data, 
but the 2dspec could be used here as well. I believe it is about the same size as the continuum (~1000 datapoints per sample)

The biggest issue here is going to be augmentations. Good augmentations already exist for images, but 1D astronomical data is not endowed with such a luxury.
Or, maybe there is a larger problem looming in the air. A beautiful thing about research is that not everything in konwn beforehand. 

Currently SwAV is being modified to accept the 1-D inputs. 
The backbone will be replaced with a stack of transformer encoders.
This approach seems valid based on the success of ViT, 
but instead of unrolling 16x16 patches of an image we will be interested in taking slices of a 1x1000 sample.
