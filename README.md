# Cubo AOLAP: Consumo Electrico Distriluz

---

## Description

This project implements an OLAP cube for analyzing electrical energy consumption data using SQL Server Analysis Services (SSAS). The cube is built on top of a dimensional database (DM_ConsumoEnergetico) that stores historical energy consumption information from Distriluz.

## Data Model

The cube consists of the following components:

### Fact Table

- `Consumo_Fact`: Contains the main metrics about energy consumption
  - `ConsumoKWh` (Energy consumption in KWh)
  - `ImporteSoles` (Amount in Peruvian Soles)
  - `HuellaCarbono` (Carbon footprint)

### Dimension Tables

- `Empresa_Dim`: Company information
  - `CompanyID`
  - `CompanyName`

- `Ubicacion_Dim`: Geographic location hierarchy
  - `Department`
  - `Province`
  - `District`
  - `UbigeoCode`

- `Tiempo_Dim`: Time dimension
  - `Year`
  - `Month`
  - `Season`

- `Cartera_Dim`: Portfolio information
  - `PortfolioDescription`
  - `TariffCode`
  - `TariffDescription`

## Features

- Multi-dimensional analysis of energy consumption
- Hierarchical navigation through dimensions
- Time-based analysis by year, month, and season
- Geographic analysis by department, province, and district
- Analysis by company and tariff types

## Technologies Used

- Microsoft SQL Server 2019
- SQL Server Analysis Services (SSAS)
- Visual Studio with SQL Server Data Tools

## Prerequisites

- SQL Server 2019 or later
- Visual Studio 2019 or later with SQL Server Data Tools
- Access to the `DM_ConsumoEnergetico` database

## Installation

1. Clone this repository.
2. Open the solution file `ProyectoMultiPFConsumoElectricoDistriluz.sln` in Visual Studio.
3. Configure the connection to your `DM_ConsumoEnergetico` database.
4. Deploy the Analysis Services project to your SSAS instance.

## Usage

Once deployed, you can analyze the data using:

- Excel with PivotTables
- Power BI
- SQL Server Management Studio
- Any other OLAP-compatible client tool

## Project Structure

``` note
ProyectoMultiPFConsumoElectricoDistriluz/ 
├── DM Consumo Energetico.cube # Main cube definition 
├── DM Consumo Energetico.ds # Data source connection 
├── DM Consumo Energetico.dsv # Data source view 
├── DM Consumo Energetico.partitions # Cube partitions 
├── Dimensions/ 
├── Cartera Dim.dim # Portfolio dimension 
├── Empresa Dim.dim # Company dimension 
├── Tiempo Dim.dim # Time dimension 
└── Ubicacion Dim.dim # Location dimension
```

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Contributors

- [David Sandoval](https://github.com/sandovaldavid)
- Team Leads:
  - Sair Bautista
  - Moises Americo
  - Jose Ramirez

## Contact

For any inquiries about this project, please contact:

### Integrante: David Sandoval

- [Email](mailto:sandovaldavid2201@gmail.com)
- [Perfil Web](https://devsandoval.me/)

---

#### Organization: Distriluz

#### Course: Business Intelligence

#### Location: Peru
