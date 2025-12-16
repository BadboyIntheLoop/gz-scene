# gz-scene

This repository contains Gazebo scene models.

## Prerequisites

### Install Gazebo Harmonic 8

Follow the official installation instructions for Gazebo Harmonic:

**Ubuntu (Debian-based):**

```bash
sudo apt-get update
sudo apt-get install lsb-release wget gnupg

# Add Gazebo repository
sudo wget https://packages.osrfoundation.org/gazebo.gpg -O /usr/share/keyrings/pkgs-osrf-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/pkgs-osrf-archive-keyring.gpg] http://packages.osrfoundation.org/gazebo/ubuntu-stable $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/gazebo-stable.list > /dev/null

# Install Gazebo Harmonic
sudo apt-get update
sudo apt-get install gz-harmonic
```

For other platforms, visit: https://gazebosim.org/docs/harmonic/install

## Installation

### 1. Clone the Repository

```bash
git clone <repository-url> gz-scene
cd gz-scene
```

### 2. Copy Model to Gazebo Directory

Copy the `vrc_driving_terrain` model to your Gazebo models directory:

```bash
cp -r vrc_driving_terrain ~/.gz/models/
```

### 3. Verify Installation

Check that the model has been copied successfully:

```bash
ls ~/.gz/models/vrc_driving_terrain
```

## Usage

Once installed, the `vrc_driving_terrain` model can be referenced in your Gazebo world files or spawned dynamically in your simulations.
