World Fertility Data Visualization Project
# An interactive visualization of global fertility trends using the World Fertility Data 2019 provided by the United Nations.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Visualization Overview](#visualization-overview)
- [Evaluation and Feedback](#evaluation-and-feedback)
- [Contributing](#contributing)
- [License](#license)
- [References](#references)

## Introduction
Understanding global fertility trends is crucial for demographic research, policy-making, and socio-economic planning. This project provides an interactive map visualization of the World Fertility Data 2019, allowing users to explore age-specific fertility rates, total fertility rates, and mean age at childbearing across different countries and over time.

## Features
- **Interactive Map Visualization**: Explore fertility indicators globally with an interactive choropleth map.
- **Multiple Indicators**: View Total Fertility Rate (TFR), Age-Specific Fertility Rate (ASFR), and Mean Age at Childbearing (MAC).
- **Temporal Analysis**: Use a slider to navigate through different years from 1950 to the present.
- **Age Group Selection**: For ASFR, select specific age groups to analyze fertility rates.
- **Responsive Design**: The map updates dynamically based on user inputs.

## Dataset
- **Source**: World Fertility Data 2019
- **Description**: Contains empirical data on fertility rates collected from civil registration systems, population censuses, and sample surveys for 201 countries or areas.
- **Citation**: United Nations, Department of Economic and Social Affairs, Population Division (2019). World Fertility Data 2019. POP/DB/Fert/Rev2019.

## Installation

### Prerequisites
- Python 3.7 or higher
- Jupyter Notebook or JupyterLab
- Git (optional, for cloning the repository)

### Clone the Repository
```bash
git clone https://github.com/DJ-Greenwood/Data_visualization.git
cd world-fertility-data-visualization
```

### Create a Virtual Environment (Optional but Recommended)
```bash
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```

### Install Required Packages
```bash
pip install --upgrade pip setuptools
pip install -r requirements.txt
```
*Note: The `requirements.txt` file includes all necessary packages such as pandas, geopandas, ipyleaflet, ipywidgets, matplotlib, etc.*

## Usage

### Download the Data Files
- Download the World Fertility Data 2019 Excel file and place it in the `data/` directory.
- Download the World Map Shapefile from Natural Earth Data and place it in the `data/Map_data/` directory.

### Run the Jupyter Notebook
1. Launch Jupyter Notebook or JupyterLab.
2. Open the `world_fertility_visualization.ipynb` notebook.
3. Run all the cells to load the data and initialize the interactive map.

### Interact with the Map
- Use the Indicator dropdown to select a fertility indicator (TFR, ASFR, MAC).
- If ASFR is selected, choose an Age Group from the corresponding dropdown.
- Adjust the Year slider to navigate through different years.
- Click on a country on the map to view detailed information in a popup.

## Project Structure
```
world-fertility-data-visualization/
├── data/
│   ├── undesa_pd_2019_world_fertility_dataset.xlsx
│   └── Map_data/
│       └── ne_110m_admin_0_countries.shp
├── images/
│   ├── TFR_visualization.png
│   ├── MAC_visualization.png
│   └── ASFR_visualization.png
├── world_fertility_visualization.ipynb
├── requirements.txt
├── README.md
└── LICENSE
```
- `data/`: Contains the fertility dataset and map shapefiles.
- `images/`: Screenshots of the visualizations.
- `world_fertility_visualization.ipynb`: The Jupyter Notebook with code and explanations.
- `requirements.txt`: List of required Python packages.
- `LICENSE`: License information for the project.

## Visualization Overview
- **Total Fertility Rate (TFR)**
- **Mean Age at Childbearing (MAC)**
- **Age-Specific Fertility Rate (ASFR)**

## Evaluation and Feedback

### Evaluation Process
- **Participants**: One English tutor and two mathematics professors.
- **Procedure**: Participants interacted with the map, exploring different regions, indicators, and time periods. Feedback was collected on usability, clarity, and effectiveness.

### Synthesis of Findings
**Positive Feedback**:
- The interactive map was intuitive and user-friendly.
- Visual representations effectively highlighted regional differences.
- The ability to select different indicators and years enhanced engagement.

**Suggestions for Improvement**:
- **Date Slider Granularity**:
    - **Issue**: The slider was too granular, cycling through days instead of years.
    - **Resolution**: Adjusted the slider to increment by years for better usability.
- **Consistency Between Datasets**:
    - **Issue**: Selected date did not remain consistent when switching indicators.
    - **Resolution**: Implemented code to retain the selected date across different datasets, defaulting to the closest available date if necessary.
- **Color Mapping Clarity**:
    - **Issue**: The color scale was challenging to interpret due to data concentration in lighter shades.
    - **Resolution**: Modified the color palette and applied data normalization techniques to enhance visual differentiation.

## Contributing
Contributions are welcome! Please follow these steps:

### Fork the Repository
Click the "Fork" button at the top right corner of this page.

### Clone Your Fork
```bash
git clone https://github.com/yourusername/world-fertility-data-visualization.git
```

### Create a New Branch
```bash
git checkout -b feature/your-feature-name
```

### Make Changes and Commit
```bash
git commit -am 'Add new feature'
```

### Push to the Branch
```bash
git push origin feature/your-feature-name
```

### Submit a Pull Request
Open a pull request explaining your changes.

## License
This project is licensed under the MIT License.

## References
- **World Fertility Data 2019**
    - United Nations, Department of Economic and Social Affairs, Population Division (2019). World Fertility Data 2019. POP/DB/Fert/Rev2019. [Data Link](https://www.un.org/development/desa/pd/data/world-fertility-data)
        - Click on the dataset lable under the Data header, to download the data. 
- **Natural Earth Data**
    - 1:110m Cultural Vectors. [Download Link](https://www.naturalearthdata.com/downloads/110m-cultural-vectors/)
- **Python Libraries**
    - [Pandas Documentation](https://pandas.pydata.org/pandas-docs/stable/)
    - [GeoPandas Documentation](https://geopandas.org/)
    - [ipyleaflet Documentation](https://ipyleaflet.readthedocs.io/en/latest/)
    - [ipywidgets Documentation](https://ipywidgets.readthedocs.io/en/latest/)
