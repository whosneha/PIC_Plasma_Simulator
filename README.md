# Exploring Plasma Simulations Using the Particle in Cell Method in 1D and 2D

# 1D Particle-in-Cell Simulation for Two-Stream Instability 

## Introduction

Welcome to the **1D Particle-in-Cell (PIC) Simulation for Two-Stream Instability** project! This project helps you understand how particles behave in a plasma—a state of matter similar to gas but with charged particles—using a computer simulation. Even if you've never coded before, this guide will walk you through what the simulation does, how it works, and how you can run it.

## What is Two-Stream Instability?

**Two-Stream Instability** happens when two groups of charged particles (like electrons) move in opposite directions through each other in one dimension. By looking at their phase space diagram we can see that any small disturbance cause a steep change in the gradient (ie the electric potential) which then snowballs into this instability effect neatly reflected in the phase space diagram. 

## What is a Particle-in-Cell (PIC) Simulation?

A **Particle-in-Cell (PIC)** simulation is a computer method used to study the behavior of charged particles in a plasma. It tracks the movement of individual particles and calculates the electric fields that influence them. This helps scientists and engineers understand complex plasma behaviors without needing to perform physical experiments.

## How Does the Simulation Work?

Here's a simple step-by-step explanation of how the simulation runs:

1. **Initialization**:
   - **Particles**: The simulation starts by placing a large number of particles randomly in a defined space.
   - **Velocities**: Half of the particles move to the right, and the other half move to the left.
   - **Perturbations**: Small changes are added to the particles' speeds to start the instability.

2. **Electric Field Calculation**:
   - The simulation calculates the electric fields created by the particles based on their positions.

3. **Movement**:
   - Using these electric fields, the simulation updates the positions and speeds of the particles.

4. **Visualization**:
   - The simulation creates visual pictures (plots) showing how the particles and electric fields change over time.

5. **Repeat**:
   - Steps 2 to 4 are repeated many times to simulate the behavior over a period.

## Getting Started

### What You Need

To run this simulation, you need:

- **Python**: A programming language. Download it from [python.org](https://www.python.org/downloads/).
- **Jupyter Notebook** (optional): A tool for running Python code interactively.
- **Python Libraries**:
  - `numpy`
  - `scipy`
  - `matplotlib`
  - `imageio`

### Installing Python and Libraries

1. **Install Python**:
   - Download and install Python from the [official website](https://www.python.org/downloads/).
   - Make sure to check the box that says "Add Python to PATH" during installation.

2. **Install Jupyter Notebook** (optional but recommended):
   - Open the Command Prompt (Windows) or Terminal (Mac/Linux).
   - Type the following command and press Enter:
     ```
     pip install notebook
     ```

3. **Install Required Libraries**:
   - In the Command Prompt or Terminal, type the following command and press Enter:
     ```
     pip install numpy scipy matplotlib imageio
     ```

### Downloading the Project

1. **Clone the Repository**:
   - If you have Git installed, open the Command Prompt or Terminal and type:
     ```
     git clone https://github.com/yourusername/two-stream-instability-pic.git
     ```
   - Replace `yourusername` with your GitHub username.

2. **Or Download as ZIP**:
   - Go to the project repository on GitHub.
   - Click on the "Code" button and select "Download ZIP".
   - Extract the ZIP file to your desired location.

### Running the Simulation

1. **Open Jupyter Notebook** (if using):
   - Navigate to the project folder in the Command Prompt or Terminal.
   - Type:
     ```
     jupyter notebook
     ```
   - This will open Jupyter in your web browser.

2. **Open the Notebook File**:
   - In Jupyter, click on the notebook file (e.g. in this case, `PIC_Plasma_Simulator.ipynb`) to open it.

3. **Run the Simulation**:
   - Inside the notebook, run each cell one by one by clicking on it and pressing `Shift + Enter`.
   - The simulation will start and display visualizations.

4. **Save Visualizations**:
   - The simulation can save animations as GIFs for you to view later.

## Understanding the Simulation Parameters

You can change how the simulation behaves by adjusting these settings:

- **Number of Particles (`num_particles`)**: How many particles are in the simulation. More particles can make the simulation more accurate but slower.
- **Number of Mesh Cells (`num_mesh_cells`)**: Divides the space into smaller sections to calculate electric fields.
- **Simulation End Time (`simulation_end_time`)**: How long the simulation runs.
- **Timestep (`time_step`)**: The size of each step in time during the simulation.
- **Domain Size (`domain_size`)**: The size of the space where particles move.
- **Electron Density (`electron_density`)**: How many electrons are in a given space.
- **Beam Velocity (`beam_velocity`)**: The speed at which particles move.
- **Beam Width (`beam_width`)**: The range of particle speeds.
- **Perturbation Amplitude (`perturbation_amplitude`)**: How much initial variation is added to particle speeds to start the instability.

You can find these settings at the beginning of the simulation code. Feel free to change them and see what happens!

## Visualization Options

The simulation provides different ways to see what's happening:

- **Phase Space Diagram**: Shows particles' positions versus their speeds. It helps you see how particles spread out or cluster together.
- **Charge Density Plot**: Displays how many particles are in each section of the space. It shows areas with high and low particle concentrations.
- **Electric Field Plot**: Illustrates the strength and direction of electric forces in different parts of the space.

You can choose which visualization to view based on what you're interested in learning.

## Customizing the Simulation

If you want to try different scenarios, you can modify the simulation in several ways:

- **Change Integration Methods**:
  - **Leapfrog**: Good for long simulations.
  - **Runge-Kutta 4th Order**: More accurate but can be slower.
  
- **Select Different Perturbations**:
  - **Sinusoidal**: Adds a wave-like variation.
  - **Cosine**: Similar to sinusoidal with a different phase.
  - **Gaussian**: Adds a bell-curve-shaped variation.
  - **Random Noise**: Adds random variations.

- **Adjust Boundary Conditions**:
  - **Periodic**: Particles exiting one side enter from the opposite side.
  - **Sticky**: Particles stick to the boundaries.
  - **Reflective**: Particles bounce back when they hit the boundaries.

## Example Runs

### Example 1: Default Settings

Run the simulation with all default settings to see the basic two-stream instability.

```python
run_simulation_1d(
    method="leapfrog",
    perturbation_type="sinusoidal",
    save_gif=True,
    visualization_mode="Phase Space"
)

```


# 2D Particle-in-Cell Simulation for Two-Stream Instability

## Introduction

Welcome to the **2D Particle-in-Cell (PIC) Simulation for Two-Stream Instability** project! This project helps you understand how particles behave in a plasma—a state of matter similar to gas but with charged particles—using a computer simulation. Even if you've never coded before, this guide will walk you through what the simulation does, how it works, and how you can run it.

## What is Two-Stream Instability?

**Two-Stream Instability** is a phenomenon that occurs when two groups of charged particles (like electrons) move in opposite directions through each other. This interaction creates waves and leads to interesting behaviors in the plasma. Understanding this instability is important in fields like astrophysics, fusion research, and electronics.

## What is a Particle-in-Cell (PIC) Simulation?

A **Particle-in-Cell (PIC)** simulation is a computer method used to study the behavior of charged particles in a plasma. It tracks the movement of individual particles and calculates the electric fields that influence them. This helps scientists and engineers understand complex plasma behaviors without needing to perform physical experiments.

## Project Overview

This simulation models the interaction between particles moving in two dimensions within a defined space. Here's a simple breakdown of how it works:

1. **Initialization**: The simulation starts by placing particles randomly in a two-dimensional space and assigning them initial speeds.
2. **Electric Field Calculation**: It calculates the electric fields generated by the particles based on their positions.
3. **Movement**: Using these electric fields, the simulation updates the positions and speeds of the particles.
4. **Visualization**: The simulation provides visual representations of how the particles and electric fields evolve over time.

Additionally, the simulation includes advanced features like injecting dense blocks of particles or simulating shock fronts to study more complex interactions.

## Getting Started

### What You Need

To run this simulation, you need:

- **Python** installed on your computer. You can download it from [python.org](https://www.python.org/downloads/).
- **Jupyter Notebook** (optional but recommended for interactive use).
- Required Python libraries:
  - `numpy`
  - `scipy`
  - `matplotlib`
  - `imageio`

### Installing Python and Libraries

1. **Install Python**:
   - Download and install Python from the [official website](https://www.python.org/downloads/).
   - Make sure to check the box that says "Add Python to PATH" during installation.

2. **Install Jupyter Notebook** (optional but recommended):
   - Open the Command Prompt (Windows) or Terminal (Mac/Linux).
   - Type the following command and press Enter:
     ```
     pip install notebook
     ```

3. **Install Required Libraries**:
   - In the Command Prompt or Terminal, type the following command and press Enter:
     ```
     pip install numpy scipy matplotlib imageio
     ```

### Downloading the Project

1. **Clone the Repository**:
   - If you have Git installed, open the Command Prompt or Terminal and type:
     ```
     git clone https://github.com/yourusername/two-stream-instability-pic-2d.git
     ```
   - Replace `yourusername` with your GitHub username.

2. **Or Download as ZIP**:
   - Go to the project repository on GitHub.
   - Click on the "Code" button and select "Download ZIP".
   - Extract the ZIP file to your desired location.

### Running the Simulation

1. **Open Jupyter Notebook** (if using):
   - Navigate to the project folder in the Command Prompt or Terminal.
   - Type:
     ```
     jupyter notebook
     ```
   - This will open Jupyter in your web browser.

2. **Open the Notebook File**:
   - In Jupyter, click on the notebook file (e.g., `simulation_2d.ipynb`) to open it.

3. **Run the Simulation**:
   - Inside the notebook, run each cell one by one by clicking on it and pressing `Shift + Enter`.
   - The simulation will start and display visualizations.

4. **Save Visualizations**:
   - The simulation can save animations as GIFs for you to view later.

## Simulation Parameters

You can change how the simulation behaves by adjusting these settings:

- **Box Dimensions**:
  - `lx`: Length of the box in the x-direction (e.g., `12` units).
  - `ly`: Length of the box in the y-direction (e.g., `3` units).

- **Grid Points**:
  - `nx`: Number of grid points along the x-axis (e.g., `50`).
  - `ny`: Number of grid points along the y-axis (e.g., `50`).

- **Particles**:
  - `num_particles`: Number of background particles (e.g., `1000`).
  - `num_dense_particles`: Number of particles injected in dense blocks or shock fronts (e.g., `5000`).

- **Physical Properties**:
  - `charge`: Charge of the particles (e.g., `1.0e-5`).
  - `mass`: Mass of the particles (e.g., `1.0e-4`).
  - `n0`: Background electron density (e.g., `1.0`).

- **Time Settings**:
  - `dt`: Time step size (e.g., `0.01` units).
  - `time_steps`: Total number of time steps (e.g., `100`).

- **Injection Parameters**:
  - `block_params`: Defines the region where particles are injected (e.g., `(8.0, 8.5, 1.0, 1.5)`).
  - `injection_interval`: When to inject particles (e.g., `10` steps).
  - `mean_velocity`: Average velocity of injected particles (e.g., `(20.0, 0.0)`).
  - `velocity_spread`: Variation in velocities of injected particles (e.g., `0.5`).
  - `shock_velocity`: Speed of the shock front (e.g., `10.0` units).
  - `shock_width`: Width of the shock front (e.g., `0.01` units).
  - `shock_force_strength`: Strength of the force applied by the shock front (e.g., `2.0`).

- **Visualization**:
  - `gif_name`: Name of the saved animation (e.g., `"simulation_2d.gif"`).
  - `visualization_mode`: Type of visualization (`"Density"`, `"Electric Field"`, etc.).

Feel free to experiment with these numbers to see different behaviors!

## How Does the 2D Simulation Work?

Here's a simple step-by-step explanation of how the 2D simulation runs:

1. **Initialization**:
   - **Particles**: The simulation starts by placing a number of particles randomly within a two-dimensional box.
   - **Velocities**: Each particle is assigned an initial speed. Background particles start with zero velocity, while injected particles have specific velocities.
   
2. **Injecting Particles**:
   - **Block Injection**: Dense groups of particles can be injected into specific regions of the box at set intervals.
   - **Shock Fronts**: Simulate moving shock fronts that interact with the background particles.

3. **Electric Field Calculation**:
   - The simulation calculates the electric fields created by the particles based on their positions on a grid.

4. **Movement**:
   - Using these electric fields, the simulation updates the positions and speeds of the particles.

5. **Boundary Conditions**:
   - **Periodic**: Particles exiting one side of the box re-enter from the opposite side.
   - **Sticky**: Particles stick to the boundaries and stop moving.
   - **Reflective**: Particles bounce back when they hit the boundaries.

6. **Visualization**:
   - The simulation creates visual pictures (plots) showing the density of particles and their positions over time.

7. **Repeat**:
   - Steps 3 to 6 are repeated for each time step to simulate the behavior over a period.

## Visualization Options

The simulation provides different ways to see what's happening:

- **Density Plot**: Shows how particles are distributed across the two-dimensional space. Areas with more particles appear brighter.

  ![Density Plot Example](density_example.png)

- **Particle Position Scatter Plot**: Displays the positions of all particles in the box at a given time step.

  ![Particle Positions Example](positions_example.png) 


**Note**: Ensure that any referenced images (like `density_example.png`) are available in your project directory for proper visualization.

## Customizing the Simulation

If you want to try different scenarios, you can modify the simulation in several ways:

- **Change Integration Methods**:
  - **Leapfrog**: Good for long simulations.
  - **Runge-Kutta 4th Order**: More accurate but can be slower.

- **Select Different Injection Methods**:
  - **Block Injection**: Injects a dense group of particles into a specific region.
  - **Shock Front**: Simulates a moving shock front that interacts with the particles.

- **Adjust Boundary Conditions**:
  - **Periodic**: Particles exiting one side enter from the opposite side.
  - **Sticky**: Particles stick to the boundaries.
  - **Reflective**: Particles bounce back when they hit the boundaries.

- **Modify Physical Properties**:
  - Change the charge and mass of particles to see how it affects the simulation.
  - Adjust the number of particles for more or less detailed simulations.

## Example Runs

### Example 1: Block Injection with Leapfrog Integration

Run the simulation by injecting a dense block of particles and using the Leapfrog integrator.

```python
run_simulation_2d(
    method="block",
    integration_method="leapfrog",
    boundary_type="periodic",
    gif_name="block_injection_leapfrog.gif"
)


