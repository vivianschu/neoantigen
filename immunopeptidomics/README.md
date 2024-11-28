# Immunopeptidomics Processing

## Installation
1. Install Mono using Homebrew:
    ```bash
    brew install mono
    ```
2. Confirm Mono installation:
    ```bash
    mono --version
    ```
3. Install [ThermoRawFileParser](https://github.com/compomics/ThermoRawFileParser/releases) from the Releases Page.
4. Download the latest `.zip` file for the parser.
5. Unzip the downloaded file to the desired location (e.g., `~/ThermoRawFileParser`)

## Convert
ThermoRawFileParser runs using the following syntax:
```bash
mono ThermoRawFileParser.exe -i=<input_file> -o=<output_directory> -f=<format>
```
### Example Command
1. Navigate to the directory where ThermoRawFileParser is located:
    ```bash
    mono ThermoRawFileParser.exe -i=/path/to/input_file.raw -o=/path/to/output_directory -f=1
    ```
2. Convert the `.raw` to `.mzML`:
    ```bash
    mono ThermoRawFileParser.exe -i=/path/to/input_file.raw -o=/path/to/output_directory -f=1
    ```
***Options***
- `-i`: Path to the input .raw file.
- `-o`: Path to the output directory.
- `-f`: Output format:
    - `0` = MGF
    - `1` = mzML
    - `2` = Indexed mzML
    - `3` = Parquet
    - `4` = No output (metadata only)

**Optional**:

Convert all `.raw` files in a directory:
```bash
mono ThermoRawFileParser.exe -d=/path/to/input_directory -o=/path/to/output_directory -f=1
```
