# Visualization Tools

Libraries and tools for visualizing Openwater data and results.

---

## Python Visualization

### Matplotlib
- **Website:** https://matplotlib.org
- **Purpose:** General-purpose plotting
- **Use Case:** Basic plots, charts, and figures
- **License:** BSD-style

**Example:**
```python
import matplotlib.pyplot as plt
import openlifu

# Plot acoustic pressure field
field = plan.compute_field()
plt.imshow(field)
plt.colorbar(label='Pressure (Pa)')
plt.show()
```

### Plotly
- **Website:** https://plotly.com/python/
- **Purpose:** Interactive plots
- **Use Case:** Web-based dashboards, interactive exploration
- **License:** MIT

**Example:**
```python
import plotly.graph_objects as go

fig = go.Figure(data=go.Heatmap(z=pressure_field))
fig.show()
```

### Seaborn
- **Website:** https://seaborn.pydata.org
- **Purpose:** Statistical visualization
- **Use Case:** Data analysis, statistical plots
- **License:** BSD

---

## 3D Visualization

### VTK (Visualization Toolkit)
- **Website:** https://vtk.org
- **Purpose:** 3D graphics and visualization
- **Use Case:** Volume rendering, 3D medical imaging
- **License:** BSD

### PyVista
- **Website:** https://docs.pyvista.org
- **Purpose:** 3D plotting (Python wrapper for VTK)
- **Use Case:** Easy 3D visualization in Python
- **License:** MIT

**Example:**
```python
import pyvista as pv

# Visualize acoustic field in 3D
mesh = pv.wrap(pressure_field_3d)
mesh.plot(cmap='viridis')
```

### Mayavi
- **Website:** https://docs.enthought.com/mayavi/mayavi/
- **Purpose:** 3D scientific visualization
- **Use Case:** Volume rendering, interactive 3D plots
- **License:** BSD

---

## Real-time Visualization

### PyQtGraph
- **Website:** https://www.pyqtgraph.org
- **Purpose:** Real-time data visualization
- **Use Case:** Live sensor data streaming
- **License:** MIT

**Example:**
```python
import pyqtgraph as pg

# Real-time blood flow display
app = pg.mkQApp()
win = pg.GraphicsLayoutWidget()
plot = win.addPlot()
curve = plot.plot()

def update(data):
    curve.setData(data)
```

---

## Medical Imaging Specific

### 3D Slicer
- **Website:** https://www.slicer.org
- **Purpose:** Medical image visualization
- **Use Case:** Treatment planning, image registration
- **License:** BSD-style

### OHIF Viewer
- **Website:** https://ohif.org
- **Purpose:** Web-based DICOM viewer
- **Use Case:** Browser-based medical image viewing
- **License:** MIT

---

## Dashboard Tools

### Dash
- **Website:** https://dash.plotly.com
- **Purpose:** Web dashboards in Python
- **Use Case:** Create web-based monitoring interfaces
- **License:** MIT

### Streamlit
- **Website:** https://streamlit.io
- **Purpose:** Quick data apps
- **Use Case:** Rapid prototyping of interfaces
- **License:** Apache 2.0

---

## Contributing

Add visualization tools you've found useful!

Format:
```markdown
### Tool Name
- **Website:** [URL]
- **Purpose:** [What it visualizes]
- **Use Case:** [When to use it]
- **License:** [License type]

**Example:** [Optional code snippet]
```

---

_Visualize your Openwater data beautifully!_ 📊
