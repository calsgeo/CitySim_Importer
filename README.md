# Dynamic energy simulations based on the 3D BAG 2.0

This repository contains the Python notebooks, SQL schemas, and sample CityGML data developed for a TU Delft MSc thesis on connecting 3D city data with [CitySim](https://www.citysimsoftware.com/) for dynamic urban energy simulations. The workflow extracts geometry and attributes from 3DCityDB, creates CitySim input files, runs simulations, and stores the results in a database with the Energy ADE extension.

## Repository contents

- `main_alderaan.ipynb` and `main_rijssenholten.ipynb`: example end-to-end CitySim workflows.
- `EPW_reader.ipynb`: converts EnergyPlus Weather (`.epw`) data to CitySim's `.cli` format.
- `DATABASE_reader.ipynb`: creates a CitySim `.cli` file from weather data stored in PostgreSQL.
- `physics_library.sql` and `weather_library.sql`: database schemas and reference data for physical properties and weather observations.
- `Alderaan.gml`, `Alderaan_DTM.gml`, and `Alderaan_Trees.gml`: sample CityGML datasets.

## Software

The notebooks were developed with Python 3 for the following software versions:

- CitySim 22.05.2022
- 3DCityDB 5.0.0
- Energy ADE 2.0
- PostgreSQL 13

Import the SQL files into PostgreSQL to install the physics and weather schemas. The sample GML files can be loaded into 3DCityDB with the 3DCityDB Importer/Exporter.

## Citation

This project started as a MSc thesis in Geomatics at TU Delft by Yuzhen Jin. For details about the method and its development, cite the associated MSc thesis. BibTeX metadata is available in [`CITATION.bib`](CITATION.bib):

> Jin, Y. (2022). *Dynamic energy simulations based on the 3D BAG 2.0* [MSc thesis, Delft University of Technology]. https://resolver.tudelft.nl/uuid:3ae123bd-cae4-45b2-be48-27ffe5cab980