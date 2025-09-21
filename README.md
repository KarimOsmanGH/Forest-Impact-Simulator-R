# Forest Impact Simulator - R Version

A comprehensive R Markdown notebook for simulating forest carbon impacts, biodiversity effects, and environmental outcomes of forest management activities.

## 🌲 Overview

The Forest Impact Simulator R notebook provides a powerful tool for analyzing the environmental impact of forest planting and clear-cutting activities. It calculates carbon sequestration/loss, biodiversity impacts, forest resilience, and generates detailed visualizations and reports.

## ✨ Features

### 📊 **Dual Mode Operation**
- **Planting Mode**: Calculates positive carbon sequestration from new forest growth
- **Clear-cutting Mode**: Calculates carbon loss from forest removal

### 📁 **Flexible Data Input**
- **CSV File Upload**: Supports structured forest data files
- **Manual Input**: Fallback option for custom data entry
- **Sample Data**: Includes example forest planting data

### 🧮 **Comprehensive Calculations**
- CO₂ impact per land plot: `CO2_impact_tons = area_ha × carbon_per_ha × years`
- Total and average metrics (totalCarbon, averageBiodiversity, averageResilience)
- Multi-year simulation support
- Environmental impact assessments

### 📈 **Rich Visualizations**
- Bar charts showing CO₂ impact/loss per land plot
- Environmental metrics comparison charts
- Area distribution pie charts
- Optional yearly carbon accumulation projections

### 💾 **Multiple Output Formats**
- **CSV Export**: Processed data for further analysis
- **JSON Export**: Web app compatible format with metadata
- **Structured Reports**: Complete environmental impact summaries

## 🚀 Quick Start

### Prerequisites

```r
# Install required R packages
install.packages(c("tidyverse", "ggplot2", "jsonlite", "readr", "dplyr", "plotly"))
```

### Basic Usage

1. **Open the notebook**: `forest-impact-simulator.Rmd`
2. **Load your data**: Either upload a CSV file or use manual input
3. **Select mode**: Choose "planting" or "clear-cutting"
4. **Run analysis**: Execute all code chunks sequentially
5. **View results**: Check the `output/` directory for generated files

### Sample Data Structure

```csv
land_id,area_ha,tree_type,carbon_per_ha,biodiversity_score,resilience_score
Plot_001,0.1,Oak,110,4.5,4.3
Plot_002,0.15,Pine,125,4.2,4.0
Plot_003,0.2,Mixed,118,4.8,4.6
```

## 📋 Data Requirements

### Required Columns
- `land_id`: Unique identifier for each land plot
- `area_ha`: Area in hectares
- `tree_type`: Type of trees/species
- `carbon_per_ha`: Carbon sequestration rate per hectare

### Optional Columns
- `biodiversity_score`: Biodiversity impact score (1-5 scale)
- `resilience_score`: Forest resilience score (1-5 scale)
- `latitude`, `longitude`: Location coordinates
- `simulation_years`: Number of years for simulation

## 🔧 Configuration

### Mode Selection
```r
# Set the simulation mode
mode <- "planting"  # or "clear-cutting"
```

### Location Parameters
```r
location_data <- data.frame(
  latitude = 50.56956736416948,
  longitude = 28.159344338632376,
  simulation_years = 50
)
```

## 📊 Output Structure

### JSON Output Format
```json
{
  "metadata": {
    "timestamp": "2025-01-XX",
    "simulatorVersion": "1.0.0",
    "location": {...},
    "simulation": {...}
  },
  "environmentalData": {
    "soil": {...},
    "climate": {...}
  },
  "impactResults": {
    "carbonSequestration": 2772.0,
    "biodiversityImpact": 4.5,
    "forestResilience": 4.5,
    "waterRetention": 94,
    "airQualityImprovement": 95,
    "totalCarbon": 122938.2,
    "averageBiodiversity": 4.5,
    "averageResilience": 4.5
  },
  "plantingData": {
    "area": 0.20,
    "totalTrees": 126,
    "spacing": 4,
    "density": 625,
    "timeline": 50,
    "plots": [...]
  }
}
```

## 📈 Example Results

### Carbon Impact Analysis
- **Total Carbon Sequestration**: 122,938.2 kg CO₂ over 50 years
- **Annual Rate**: 2,772 kg CO₂/year
- **Area Coverage**: 0.20 hectares
- **Tree Density**: 625 trees/hectare

### Environmental Metrics
- **Average Biodiversity Impact**: 4.5/5
- **Forest Resilience**: 4.5/5
- **Water Retention**: 94%
- **Air Quality Improvement**: 95%

## 🎯 Use Cases

### Research & Academia
- Forest carbon studies
- Environmental impact assessments
- Biodiversity research
- Climate change mitigation analysis

### Conservation Organizations
- Reforestation project planning
- Environmental monitoring
- Impact reporting
- Stakeholder communications

### Government & Policy
- Environmental policy development
- Carbon credit calculations
- Land use planning
- Regulatory compliance

### Corporate Sustainability
- ESG reporting
- Carbon footprint analysis
- Sustainability initiatives
- Environmental risk assessment

## 🔬 Scientific Methodology

### Carbon Calculations
- Based on species-specific carbon sequestration rates
- Linear accumulation model over simulation period
- IPCC-compliant carbon accounting methods
- Adjustable for different growth patterns

### Environmental Metrics
- Biodiversity scoring based on species diversity
- Resilience assessment using ecological indicators
- Water retention calculated from forest structure
- Air quality improvement from particulate filtration

## 📚 Dependencies

```r
# Core data manipulation
library(tidyverse)
library(dplyr)
library(readr)

# Visualization
library(ggplot2)
library(plotly)

# Data export
library(jsonlite)

# Markdown rendering
library(knitr)
library(rmarkdown)
```

## 🤝 Contributing

We welcome contributions to improve the Forest Impact Simulator R notebook:

1. **Fork the repository**
2. **Create a feature branch**
3. **Make your changes**
4. **Add tests if applicable**
5. **Submit a pull request**

### Development Guidelines
- Follow R coding best practices
- Include comprehensive documentation
- Test with various data inputs
- Maintain backward compatibility

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🔗 Related Projects

- **Python Version**: [Forest-Impact-Simulator-Python](https://github.com/KarimOsmanGH/Forest-Impact-Simulator-Python)
- **Web Application**: Forest Impact Simulator Web App
- **Documentation**: [Forest Impact Analysis Guide](https://github.com/KarimOsmanGH/Forest-Impact-Simulator-R/wiki)

## 📞 Support

### Getting Help
- **Issues**: Report bugs or request features via [GitHub Issues](https://github.com/KarimOsmanGH/Forest-Impact-Simulator-R/issues)
- **Discussions**: Join community discussions in [GitHub Discussions](https://github.com/KarimOsmanGH/Forest-Impact-Simulator-R/discussions)
- **Documentation**: Check the [Wiki](https://github.com/KarimOsmanGH/Forest-Impact-Simulator-R/wiki) for detailed guides

### Common Issues
- **Data Format**: Ensure CSV files match the required column structure
- **Package Dependencies**: Install all required R packages before running
- **Memory Issues**: For large datasets, consider processing in smaller chunks

## 🌟 Acknowledgments

- **Forest Research Community**: For carbon sequestration data and methodologies
- **R Community**: For excellent packages and documentation
- **Environmental Scientists**: For validation and feedback
- **Open Source Contributors**: For continuous improvements

## 📊 Version History

### v1.0.0 (Current)
- Initial release with core functionality
- Planting and clear-cutting modes
- CSV and JSON output support
- Comprehensive visualizations
- Sample data included

### Roadmap
- **v1.1.0**: Enhanced visualization options
- **v1.2.0**: Additional environmental metrics
- **v1.3.0**: Machine learning integration
- **v2.0.0**: Web interface integration

---

**Made with 🌱 for the environment**

*Forest Impact Simulator R - Empowering data-driven forest management decisions*
