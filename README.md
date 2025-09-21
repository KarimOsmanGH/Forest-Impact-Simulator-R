# Forest Impact Simulator - R Version

R notebook to simulate the impact of forest management

## About

A comprehensive R Markdown notebook for simulating forest carbon impacts, biodiversity effects, and environmental outcomes of forest planting and clear-cutting activities.

## Features

- **Planting Mode**: Calculate positive carbon sequestration from new forest growth
- **Clear-cutting Mode**: Calculate carbon loss from forest removal
- **CSV File Upload**: Support for structured forest data files
- **Manual Input**: Fallback option for custom data entry
- **Visualizations**: Bar charts, pie charts, and environmental metrics
- **Multiple Outputs**: CSV and JSON export formats

## Quick Start

1. Install required R packages:
```r
install.packages(c("tidyverse", "ggplot2", "jsonlite", "readr", "dplyr", "plotly"))
```

2. **Get CSV Data** (Optional): Visit [Forest Impact Simulator Web App](https://forest-impact-simulator.vercel.app/) to run a simulation and download CSV data, or use the included sample data

3. Open `forest-impact-simulator.Rmd` in RStudio

4. Run all code chunks to perform the analysis

5. Check the `output/` directory for generated files

## Data Format

The notebook supports two input formats:

### Structured CSV Format (Recommended)
Upload a CSV file with the following sections:
- **METADATA**: Timestamp, simulator version, simulation years, location coordinates
- **SELECTED TREES**: Tree name, scientific name, carbon sequestration rate, percentage
- **ENVIRONMENTAL DATA**: Soil carbon, pH, temperature, precipitation
- **IMPACT RESULTS**: Annual carbon sequestration, total carbon, biodiversity, resilience
- **PLANTING DATA**: Area, total trees, spacing, density

**💡 Get CSV Format**: You can generate the proper CSV format by running a simulation on the [Forest Impact Simulator Web App](https://forest-impact-simulator.vercel.app/) and downloading the results. The web app will export data in the exact format required by this R notebook.

### Manual Input Format
If no CSV file is available, use manual input with these columns:
- `land_id`: Unique identifier for each land plot
- `area_ha`: Area in hectares
- `tree_type`: Type of trees/species
- `carbon_per_ha`: Carbon sequestration rate per hectare

Optional columns:
- `biodiversity_score`: Biodiversity impact score (1-5 scale)
- `resilience_score`: Forest resilience score (1-5 scale)

## Usage

```r
# Set simulation mode
mode <- "planting"  # or "clear-cutting"

# Configure location and years
location_data <- data.frame(
  latitude = 50.56956736416948,
  longitude = 28.159344338632376,
  simulation_years = 50
)
```

## Output

The notebook generates:
- **CSV file**: Processed forest data
- **JSON file**: Web app compatible format
- **Visualizations**: Charts showing CO₂ impact and environmental metrics

## Related Projects

- **Python Version**: [Forest-Impact-Simulator-Python](https://github.com/KarimOsmanGH/Forest-Impact-Simulator-Python)
- **TypeScript Version**: [Forest-Impact-Simulator](https://github.com/karimosmanGH/Forest-Impact-Simulator)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
