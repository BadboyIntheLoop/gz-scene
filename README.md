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
git clone http://gitlab.s/chungnt.s/gz-scene.git gz-scene
cd gz-scene
```

### 2. Copy Models to Gazebo Directory

Copy all models to your Gazebo models directory:

```bash
cp -r */ ~/.gz/models/
```

### 3. Verify Installation

Check that the models have been copied successfully:

```bash
ls ~/.gz/models/
```

## Updated Models

### baylands
This local version replaces the Ogre 1.x scripts with ogre2-compatible PBR materials (`<pbr><metal><albedo_map>`), while keeping the mesh files referenced from Gazebo Fuel. To update the baylands model in your Gazebo Fuel cache:

```bash
cp baylands/model.sdf ~/.gz/fuel/fuel.gazebosim.org/openrobotics/models/baylands/3/model.sdf
cp baylands/model.config ~/.gz/fuel/fuel.gazebosim.org/openrobotics/models/baylands/3/model.config
```

## Usage

Once installed, the models can be referenced in your Gazebo world files or spawned dynamically in your simulations.
