# Analysis Libraries

Data processing and analysis tools for Openwater platforms.

---

## Numerical Computing

### NumPy
- **Website:** https://numpy.org
- **Purpose:** Numerical computing fundamentals
- **Use Case:** Array operations, linear algebra
- **License:** BSD

**Example:**
```python
import numpy as np

# Calculate focal depth
depths = np.linspace(0, 100, 1000)
pressures = compute_pressure(depths)
focal_depth = depths[np.argmax(pressures)]
```

### SciPy
- **Website:** https://scipy.org
- **Purpose:** Scientific computing
- **Use Case:** Optimization, signal processing, statistics
- **License:** BSD

**Example:**
```python
from scipy.signal import butter, filtfilt

# Filter motion sensor data
b, a = butter(4, 0.1)
filtered_data = filtfilt(b, a, raw_data)
```

---

## Signal Processing

### PyWavelets
- **Website:** https://pywavelets.readthedocs.io
- **Purpose:** Wavelet transforms
- **Use Case:** Time-frequency analysis
- **License:** MIT

### librosa
- **Website:** https://librosa.org
- **Purpose:** Audio and signal analysis
- **Use Case:** Spectral analysis, feature extraction
- **License:** ISC

---

## Medical Image Processing

### SimpleITK
- **Website:** https://simpleitk.org
- **Purpose:** Image registration, segmentation
- **Use Case:** Medical image preprocessing
- **License:** Apache 2.0

**Example:**
```python
import SimpleITK as sitk

# Register CT to MRI
fixed = sitk.ReadImage('ct.nii')
moving = sitk.ReadImage('mri.nii')
registered = sitk.Elastix(fixed, moving)
```

### scikit-image
- **Website:** https://scikit-image.org
- **Purpose:** Image processing
- **Use Case:** Segmentation, feature extraction
- **License:** BSD

---

## Machine Learning

### scikit-learn
- **Website:** https://scikit-learn.org
- **Purpose:** Machine learning
- **Use Case:** Classification, regression, clustering
- **License:** BSD

**Example:**
```python
from sklearn.ensemble import RandomForestClassifier

# Classify treatment outcomes
model = RandomForestClassifier()
model.fit(features, outcomes)
prediction = model.predict(new_features)
```

### TensorFlow / PyTorch
- **TensorFlow:** https://tensorflow.org
- **PyTorch:** https://pytorch.org
- **Purpose:** Deep learning
- **Use Case:** Neural networks, advanced ML
- **License:** Apache 2.0 / BSD

---

## Statistical Analysis

### pandas
- **Website:** https://pandas.pydata.org
- **Purpose:** Data manipulation and analysis
- **Use Case:** Data cleaning, analysis, aggregation
- **License:** BSD

**Example:**
```python
import pandas as pd

# Analyze treatment results
df = pd.DataFrame(results)
summary = df.groupby('treatment_type').agg({
    'pressure': 'mean',
    'outcome': 'count'
})
```

### statsmodels
- **Website:** https://www.statsmodels.org
- **Purpose:** Statistical models
- **Use Case:** Regression, time series, hypothesis testing
- **License:** BSD

---

## Optimization

### scipy.optimize
- **Part of:** SciPy
- **Purpose:** Optimization algorithms
- **Use Case:** Parameter optimization, fitting
- **License:** BSD

**Example:**
```python
from scipy.optimize import minimize

# Optimize transducer parameters
def objective(params):
    return -compute_focal_pressure(params)

result = minimize(objective, initial_params)
optimal_params = result.x
```

---

## Acoustic Analysis

### acoustics (python-acoustics)
- **Website:** https://python-acoustics.github.io
- **Purpose:** Acoustics analysis
- **Use Case:** Sound field analysis
- **License:** BSD

---

## Biomedical Signal Processing

### BioSPPy
- **Website:** https://biosppy.readthedocs.io
- **Purpose:** Biosignal processing
- **Use Case:** ECG, EMG, EEG analysis
- **License:** BSD

### HeartPy
- **Website:** https://python-heartrate-analysis-toolkit.readthedocs.io
- **Purpose:** Heart rate analysis
- **Use Case:** Cardiovascular signal processing
- **License:** MIT

---

## Contributing

Add analysis libraries you've found useful!

Format:
```markdown
### Library Name
- **Website:** [URL]
- **Purpose:** [What it does]
- **Use Case:** [When to use it]
- **License:** [License type]

**Example:** [Optional code snippet]
```

---

_Powerful analysis tools for Openwater data!_ 🔬
