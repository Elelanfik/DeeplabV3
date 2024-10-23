# DeeplabV3

DeepLab is a series of image semantic segmentation models that excels at capturing both global context (understanding large objects) and fine details ( accurately delineating boundaries).
Deeplab variant
DeeplabV1

This model introduced Atrous convolution(AC) that prevents down sampling and increases the receptive field in 2015.
2. DeeplabV2
It added Atrous spatial pyramid pooling(ASPP) for multiscale context aggregation in 2016.
3. DeeplabV3
improved ASSP by adding batch normalization and removing CRF and lunch in 2017.
4. Deeplabv3+
combined deeplabV3 with explicit decoder which helps recover sharp object boundaries, leading to improved performance.
Key concepts (Key component of deeplab)
Atrous Convolution (Dilated Convolution): AC is a form of conv operation that inserts holes (dilation) between filter weights that allow increasing the receptive field without increasing the number of parameters (decreasing the resolution of feature maps).
AC allows Deeplab to maintain a high-resolution while still capturing wide contextual information which is essential for understanding objects at different scales.
Atrous Spatial Pyramid Pooling(ASPP): It is core component of Deeplab which is designed to capture multiscale information effectively.
applies AC with different rates (dilation factors) in parallel, allowing the model to look at images simultaneously at different scales.
ASSP applies AC with varying dilation rates in parallel and then concatenates the resulting feature maps. This technique helps in aggregating information from different view, making it easier to recognize objects at various size
