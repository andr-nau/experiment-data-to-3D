# experiment-data-to-3D
__Exprimental data processing to make 3D picture__

__Goal:__ to prepare the set of measured data (current vs. voltage vs. magnetic field) for 3D presentation.

1. To center a current-voltage (I-V) curve relatively to the (0.0) coordinates
2. To cut an interesting part of I-V
3. To prepare XYZ data set, or matrix representation. Configuration: X - voltage, Y - magnetic field, Z - current

__Workflow:__

Initially, an output from the experiment is current vs. voltage dependence, or I-V curve. Typical look of I-V curve for superconducting aluminum nanowire is shown on Fig.1.

![Fig.1](https://github.com/andr-nau/experiment-data-to-3D/blob/master/Fig1.gif "IV")

It could be not clearly visible, but IV is shifted a little bit from X=0 line, as well as from Y=0 line. See zoomed picture of superconducting vertical part of IV on Fig.2:

![Fig.2](https://github.com/andr-nau/experiment-data-to-3D/blob/master/Fig2.gif "IV zoom")
