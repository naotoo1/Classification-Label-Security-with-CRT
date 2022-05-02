# Classification-Label-Security-Certainty

## What is it?
Classification label security determines the extent to which predicted labels from classification results can be trusted. The uncertainty surrounding classification labels is resolved by the security to which the classification is made. Therefore, classification label security is very significant for decision-making whenever we are encountered with a classification task.

## File structure

```
.
├── contour.py                               # Visualization of plots
├── crt.py                                   # optimised algorithm for multiple reject thresholds for improving classification reliability
├── crt_chow_iris.py                         # simulation of crt vs chow in optimal search of for threshold for improving classification reliability
├── iris_securitycelvq.py                    # Iris_test set example with celvq
├── iris_securityglvq.py                     # Iris_test set example with glvq
├── iris_securitygmlvq.py                    # Iris_test set example with gmlvq
├── iris_securitycelvq.py                    # Iris_test set example with celvq
├── procertnew.py                            # auxilliary script for crt usage
├── label_security1.py                       # classification label security/certainty for lvq
├── protocert.py                             # Auxilliary code
└── README.md
```

## How to use?
This implementation investigates the determination of the classification label security by utilizing fuzzy probabilistic assignments of Fuzzy c-means.
The ```label_security1.py``` script is used for computing the classification label security of lvq with examples for **GLVQ**, **GMLVQ** and **CELVQ** models.

The models are first trained using a training data and tested on a test data. So for every prediction from the models using a test data, the code returns the classification labels and their respective security/certainty.

The module is imported with the **LabelSecurity Class** ,**LabelSecurityM Class** and **LabelSecurityLM Class** which is used to the compute the classification label security by calling on the methods in these Classes. LabelSecurity Class is used for **non matrix LVQ**, LabelSecurityM used for **matrix LVQ** and LabelSecurityLM used for **localized matrix LVQ**

Examples are shown in the following python files (```Iris_security_glvq.py```, ```Iris_security_gmlvq.py``` and  ```Iris_security_celvq.py```)



## Visualization / Results

Classification results with reject and non-reject options based on the chow's approach (out of a simulated test results with a security thresh-hold of 0.7)  is shown below for the GLVQ, GMLVQ and CELVQ models respectively.

<p style='align:center'>
<img src='https://user-images.githubusercontent.com/82911284/165191983-dead7c3c-30b7-4f68-bc57-3e608df501bb.png'/>
</p>

<p style='align:center'>
<img src='https://user-images.githubusercontent.com/82911284/165192166-f6cf594c-c50c-4ef8-9777-7636e954f94e.png'/>
</p>

<p style='align:center'>
<img src='https://user-images.githubusercontent.com/82911284/165192342-45d9fc5a-93d9-4d14-8be3-b2d281032af5.png'/>
</p>

## Simulation

A simulated results from multiple reject thresholds for improving classification reliability using the CRT vs Chow is shown below for GLVQ

![Figure_4](https://user-images.githubusercontent.com/82911284/165868376-edfd75fd-dc67-41f1-a75a-305f2a72e06f.png)


## References

<a id="1">[1]</a> 
Fumera, G., Roli, F., & Giacinto, G. (2000, August). 
Multiple reject thresholds for improving classification reliability. 
In Joint IAPR International Workshops on Statistical Techniques in Pattern Recognition (SPR) and Structural and Syntactic Pattern Recognition (SSPR) (pp. 863-871). Springer, Berlin, Heidelberg.
