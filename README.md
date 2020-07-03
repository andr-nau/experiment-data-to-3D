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

Centering IV is crucial for extracting information from it (positions of switching and retrapping point), and for recalculating it in different units (R-I, resistance- current representation). So, the first step is to center an IV at (0,0) position. 

For this I developed a Python code [IV_processing_Python](https://github.com/andr-nau/IV_processing_python). It works also in batch mode for large amount of experimental files. On the output this code gives set of files with centered, rescaled and recalculated IVs, as well as positions of critical points (switching/retrapping). 

Fig.3 shows visualisation from the python code during shifting procedure:

![Fig.3](https://github.com/andr-nau/experiment-data-to-3D/blob/master/Fig3.png "IV shift")

Next, using additional Mathematica code, I cut IVs to show only retrapping part (what I'm interested in) at I quadrant (+,+):

![Fig.4](https://github.com/andr-nau/experiment-data-to-3D/blob/master/Fig4.gif "IV cut")

Some repetitive features on the curves are clearly visible. But it appeared that curves first move up and then move down. So, the best representation could be in 3D. Using the same Mathematica code, I prepared XYZ file for 3D presentation, see Fig.5:

![Fig.5](https://github.com/andr-nau/experiment-data-to-3D/blob/master/Fig4.gif "IV 3D")

Now it is clearly visible all curvature, that appear due to magnetic field changes.
