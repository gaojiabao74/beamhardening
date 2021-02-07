# beamhardening
Applies a beam hardening correction on a given tif sequence

##  simple
Correction is calculated on one given slide only

**Inputs**:
 - z             = slice to use for correction, z >= 1
 - input_folder  = folder where the original tif sequence is stored
 - output_folder = folder where the corrected tif sequence will be stored
 - angle_ini     = initial angle for angle range for radial profile. Angle in
degrees: 0 is 12:00 and 90 is 3:00
 - angle_fin     = final anle for angle range for radial profile (degrees)


## **How to use it**
**1. Install the following python libraries:**
- numba
- scipy
- cv2
- sectorizedradialprofile

*sectorizedradialprofile* can be found here: [link](https://pypi.org/project/sectorizedradialprofile/)

**2. Download the beamhardening.py**
In your working folder download the file *beamhardening.py*

**3. Store the input tif sequence in an appropriate folder**
In your working directory create an input folder (i.e. *input*) and store your original tif sequence

**4. Code example**
```
>>> import beamhardening as bh

>>> bh.simple(100, input_folder = 'input')

```

In the code above, *100* is the slice you want to use to calibrate the correction

**5. Output**
An output folder containing the corrected tif sequence will be created in your working directory
