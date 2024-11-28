# Immunopeptidomics Processing

## Installation
1. If on MacOS, follow instructions to install [Docker](https://docs.docker.com/desktop/setup/install/mac-install/).
2. Pull the docker image to convert vendor data by [ProteoWizard]().
    ```bash
    docker pull chambm/pwiz-skyline-i-agree-to-the-vendor-licenses
    ```

# Convert
3. Convert all the files in your data folder. The converted mzML will be contained in the same directory of your raw data folder.
    ``` bash
    docker run -it --rm -e WINEDEBUG=-all -v /your/data/path/:/data chambm/pwiz-skyline-i-agree-to-the-vendor-licenses wine msconvert /data/*.RAW
    ```

