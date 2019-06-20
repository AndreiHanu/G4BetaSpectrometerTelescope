# G4BetaSpectrometerTelescope

## Authors

* Andrei R. Hanu (hanua at mcmaster.ca), McMaster University, Hamilton, Ontario, Canada

## Description

Describe the application here.

## Release History

0.0 - Initial Release

## Build Notes
To build this application, you should have a working version of CMake and Geant 4.10.3.p01 or higher.

Geant4: https://geant4.web.cern.ch/geant4/ CMake: https://cmake.org/

I recommend setting up your directory structure as follows:

- $G4WORKDIR/G4BetaSpectrometerTelescope : This is the source directory and is a clone of the code from this GitHub 
- $G4WORKDIR/G4BetaSpectrometerTelescope-build : Contains directories and files for each build. This directory also contains the executable files and example macros.

The simulation works both in sequential and in multi-threaded (MT) modes of Geant4. However, a significant speedup can be achieved by running the simulation in MT mode.

## Steps to compile:
### Step 1 - Source the Geant4 environment setup script

    source /opt/Geant4/geant4.10.03.p01-install/bin/geant4.sh

### Step 2 - Create the build directory and navigate to it
    
    mkdir G4BetaSpectrometerTelescope-build && cd $_

### Step 3 - Setup CMake, make the build, and run the build

    sudo cmake -DGeant4_DIR=/opt/Geant4/geant4.10.03.p01-install/lib/Geant4-10.3.1/ ~/G4WORK/G4BetaSpectrometerTelescope; sudo make -j8; ./G4BetaSpectrometerTelescope


To recompile, I recommend just re-running the command in Step 3

## Scoring Physical Quantities
Describe any physical quantities (e.g. energy, time-of-arrival, etc.) that are scored and the data format in which they are stored.
