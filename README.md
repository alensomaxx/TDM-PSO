# README.md for TDM-PSO Simulation Package

## 🧠 Time-Decaying Memory PSO (TDM-PSO) for Multi-Robot Coordination

This ROS + Gazebo simulation package demonstrates the patented TDM-PSO algorithm for adaptive multi-robot coordination in dynamic environments. The system shows how incorporating time-decaying memory improves over standard PSO in terms of collision avoidance, adaptability, and path efficiency.

---

## 📦 Features
- Simulates 10 TurtleBot3 robots
- Dynamic warehouse environment with moving obstacles
- PSO and TDM-PSO velocity updates
- Real-time ROS logging per robot
- Automated evaluation + plots

---

## 🚀 Quick Start

### 1. Prerequisites
- ROS Noetic
- Gazebo (v11)
- Ubuntu 20.04
- `turtlebot3_gazebo` installed

### 2. Setup
```bash
mkdir -p ~/tdm_pso_ws/src
cd ~/tdm_pso_ws/src
# Place the contents of this repo here
cd ..
catkin_make
source devel/setup.bash
export TURTLEBOT3_MODEL=burger
```

### 3. Launch Simulation
```bash
roslaunch tdm_pso launch_all_sim.launch
```

### 4. View Performance Plots
```bash
cd ~/tdm_pso_ws/src/tdm_pso/scripts
python3 evaluation.py
```

---

## 📂 Folder Structure
```
tdm_pso_ws/src/tdm_pso/
├── launch/
│   ├── launch_all_sim.launch
│   ├── spawn_robots.launch
│   └── delay.launch
├── scripts/
│   ├── pso_node.py          # Standard PSO
│   ├── tdm_pso_node.py      # Time-Decaying PSO
│   ├── logger_node.py       # Per-robot logging
│   └── evaluation.py        # Post-run analysis
├── worlds/
│   └── warehouse.world      # Dynamic obstacle map
├── logs/                    # Auto-generated metrics
```

---

## 📈 Metrics Logged
- 🧮 Path Length
- ⏱️ Time to Goal
- 🚧 Collisions

All results saved to `logs/` in CSV format per robot.

---

## 📄 Citation / Patent
If you use this system in academic or commercial work, please cite:

**Patent Title**: Time-Decaying Memory Particle Swarm Optimization for Multi-Robot Coordination  
**Inventors**: Alen Alex, Tirumala Sri Ampolu, Jowan Joe Mathew, Thomas Prinil, Nikita Singla  
**Institution**: Lovely Professional University  
**Patent Status**: Filed  

---

## 🙌 Acknowledgements
Thanks to the mentors, test users, and reviewers involved in the early phases of this project.

---

## 🛠️ To-Do / Future Work
- [ ] Add Soft Actor-Critic to auto-tune decay constant
- [ ] Test with real TurtleBot hardware
- [ ] Improve dynamic obstacle realism

---

## 📬 Contact
For queries, reach out to Alen Alex: [alensocreations@gmail.com](mailto:alensocreations@gmail.com)
