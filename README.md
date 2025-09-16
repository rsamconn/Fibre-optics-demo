# Data Analysis - Irradiation of a Fibre Optic Sensor
Measuring humidity in radioactive environments is challenging because, as you might expect, the radiation is massively damaging to sensors. Most commercial humidity sensors are electronic and get wiped out by even a small dose of radiation. 
<!-- This presents a problem for measuring humidity in many environments with high radiation - in space, in nuclear industries and in high energy physics experiments. -->
<!-- (What commercial sensors?
How much radiation kills them??) -->

However, recently a new type of technology has emerged for these cases - fibre optic sensors (FOS). These can survive radiation doses up to the Mega-Gray (MGy) level while still giving a clear signal. Even better, the change in the signal itself can actually be used to measure the radiation dose. Combined with recent breakthroughs in FOS for measuring humidity, these sensors present an exciting potential product with applications in areas such as:
- **Nuclear reactors and nuclear waste**
- **Space Technology**
- **High Energy Physics**
<!-- Link to FOS radiation studies
Link to LPG humidity studies
How much damage would MGy do to a person? -->

This project will take you through analysis of a sensor under irradiation, using real data recorded at the [PS-IRRAD facility](https://ps-irrad.web.cern.ch/ps-irrad/) in CERN, Geneva, Switzerland.

## Analysis Highlights
- **Data Processing**: Parsing and sampling of large spectroscopic datasets
- **Signal Analysis**: Time-evolution of spectral features during irradiation using `pandas` and `numpy`
- **Visualization**: Spectral plots showing radiation-induced changes using `matplotlib`
- **Insights**: Correlation between spectral shifts and radiation dose

## Running the Analysis
The data comes pre-processed to fit into 4 files totalling just over 10 MB.

Once the necessary Python packages are installed, all that is required is to run the notebook cells

### Commands
Install the necessary python packages:
```bash
git clone https://github.com/rsamconn/Fibre-optics-demo.git
```

Clone this repository:
```bash
pip install pandas numpy matplotlib datetime jupyter
```

### Project Structure
```
├── irrad-demo-data/
│   ├── times.txt                                       # A series of time values in seconds
│   ├── spectra.txt                                     # A series of spectra, each containing 20,000 points
│   ├── SEC_data_06-11_09_2023.csv                      # Data from the PS-IRRAD facility recording the dose rate over time
│   └── hyperion-transmission-spectrum.txt              # A single spectrum, used as a baseline
├── fiber_optic_analysis.ipynb                          # Main analysis notebook
├── README.md                                           # This file
└── requirements.txt                                    # Python dependencies
```