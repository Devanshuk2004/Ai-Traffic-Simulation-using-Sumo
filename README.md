# Ai-Traffic-Simulation-using-Sumo


This project demonstrates an AI-driven traffic simulation system that leverages SUMO, OSMnx, TraCI, and SUMOLib to dynamically manage traffic signals. The simulation uses a real-world map of Panaji, Goa, extracted using OSMnx, and applies traffic logic to optimize traffic flow at intersections.

# **Features**

Map Integration: Utilizes OSMnx to fetch the map of Panaji, Goa, and converts it for use in SUMO.

Dynamic Traffic Signal Control: Employs custom logic to manage traffic lights based on real-time traffic conditions.

Specialized Green Passage Logic: Activates green passage dynamically to alleviate congestion at a specific junction.

TraCI and SUMOLib Integration: Uses TraCI and SUMOLib to control and monitor traffic simulation in real-time.

Realistic Traffic Flow Simulation: Mimics real-world traffic patterns, including main and side road prioritization.

# **Work Done**

**Data Mining:**

Map Extraction: Utilized OSMnx to extract the road network map for Panaji, Goa.

Preprocessing: Converted OSMnx output to SUMO-compatible network files.

Traffic Logic Implementation:

Developed Python scripts for traffic signal management using TraCI and SUMOLib.

Configured dynamic thresholds for vehicle counts to manage traffic flows efficiently.

Added functionality to prioritize traffic at special junctions experiencing congestion.

Real-Time Monitoring:

Integrated real-time simulation capabilities using SUMO GUI.

Applied downstream lane control for propagating green signals to manage traffic holistically.

# **Prerequisites**

SUMO: Install SUMO traffic simulator. Ensure sumo-gui is available.

Python Libraries: Install the following Python libraries:

osmnx

sumolib

traci

time

Map Configuration: Generate the Panaji map using OSMnx and convert it to SUMO-compatible files.

**Code Overview
**
Parameters

Thresholds:

threshold_cars: Minimum vehicles to maintain priority phase.

congestion_threshold: Trigger green passage during heavy congestion.

# **Durations:**
green_time_main: Green signal time for the main road.

green_time_side: Green signal time for the side road.

yellow_time: Yellow signal duration.

green_passage_duration: Duration of the green passage.
**
Special Junction Logic:**

special_junction_id: ID of the junction for special green passage logic.

Downstream Control:

lookahead_range: Number of downstream signals considered for propagation.

# **Key Functions**

get_downstream_lanes(lane_ids): Retrieves downstream lane connections.

activate_green_passage(junction_id, controlled_lanes): Activates green passage for a junction and propagates it to downstream lanes.

manage_traffic(): Manages traffic signals dynamically based on vehicle counts and predefined thresholds.
**
Repository Structure**

data: Contains map files and configuration files for SUMO.

scripts: Includes Python scripts for traffic simulation and signal management.

outputs: Contains simulation results and logs.

notebooks: Jupyter notebooks for analysis and visualization.
