# 🎯 AI Pathfinding Visualizer

An interactive web-based visualization tool for comparing five fundamental pathfinding algorithms: A* (A-Star), Dijkstra's algorithm, Breadth-First Search (BFS), Depth-First Search (DFS), and Q-Learning reinforcement learning.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Demo](#demo)
- [Installation](#installation)
- [Usage](#usage)
- [Algorithms](#algorithms)
- [Performance Comparison](#performance-comparison)
- [Technologies](#technologies)
- [Project Structure](#project-structure)
- [Research Paper](#research-paper)
- [Contributing](#contributing)
- [License](#license)
- [Author](#author)

## 🌟 Overview

This project presents a comprehensive interactive web-based visualization system that enables direct comparison of five distinct pathfinding approaches. The visualizer provides real-time animation of algorithm execution on a customizable 30×30 grid environment, allowing users to draw obstacles and observe how different algorithms navigate to find optimal or near-optimal paths.

### Key Highlights

- ✅ **5 Algorithms**: A*, Dijkstra, BFS, DFS, and Q-Learning
- ✅ **Real-time Visualization**: Watch algorithms explore the grid step-by-step
- ✅ **Interactive Grid**: Draw custom obstacles and set start/end points
- ✅ **Performance Metrics**: Compare cells visited, path length, and execution time
- ✅ **Machine Learning**: Q-Learning trains for 500 episodes using reinforcement learning
- ✅ **Educational Tool**: Perfect for learning algorithm behavior and trade-offs

## ✨ Features

### Interactive Controls
- 🟩 **Set Start Point**: Click to place the green start position
- 🟥 **Set End Point**: Click to place the red destination
- 🧱 **Draw Walls**: Click and drag to create black obstacles
- 🗑️ **Erase**: Remove walls or reset points
- ↩️ **Clear Path**: Remove visualization while keeping the grid
- 🔄 **Reset All**: Start fresh with an empty grid

### Algorithm Options
- 🚀 **A* Algorithm**: Optimal & efficient with Manhattan distance heuristic
- 📊 **Dijkstra**: Guaranteed shortest path with uniform exploration
- 🌊 **BFS**: Layer-by-layer breadth-first search
- 🌲 **DFS**: Deep exploration with depth-first search
- 🧠 **Q-Learning**: Reinforcement learning with 500 training episodes

### Visual Feedback
- **Green Cells**: Start point
- **Red Cells**: End point
- **Black Cells**: Walls/obstacles
- **Light Blue Cells**: Visited during search
- **Yellow Cells**: Final optimal path
- **Real-time Stats**: Algorithm name, cells visited, path length, execution time

## 🎥 Demo

### Screenshots

#### Main Interface
![Main Interface](screenshots/interface.png)

#### A* Algorithm Execution
![A* Algorithm](screenshots/astar.png)

#### Q-Learning Training
![Q-Learning](screenshots/qlearning.png)

## 🚀 Installation

### Option 1: Direct Download (Recommended)

```bash
# Clone the repository
git clone https://github.com/yourusername/ai-pathfinding-visualizer.git

# Navigate to the project directory
cd ai-pathfinding-visualizer

# Open index.html in your browser
# No build process or dependencies needed!
```

### Option 2: Using Live Server (VS Code)

```bash
# Install Live Server extension in VS Code
# Then right-click on index.html and select "Open with Live Server"
```

### Option 3: Simple HTTP Server

```bash
# Using Python 3
python -m http.server 8000

# Using Python 2
python -m SimpleHTTPServer 8000

# Then open http://localhost:8000 in your browser
```

### Option 4: Using Node.js

```bash
# Install http-server globally
npm install -g http-server

# Run server
http-server

# Open http://localhost:8080 in your browser
```

## 📖 Usage

### Quick Start Guide

1. **Set Up the Grid**
   ```
   - Click "Set Start" button
   - Click any cell on the grid (turns GREEN)
   - Click "Set End" button
   - Click another cell (turns RED)
   ```

2. **Create Obstacles**
   ```
   - Click "Draw Walls" button
   - Click and DRAG on the grid to draw black obstacles
   - Create mazes, corridors, or random patterns
   ```

3. **Run Algorithms**
   ```
   - Click any algorithm button (A*, Dijkstra, BFS, DFS, or Q-Learning)
   - Watch the real-time visualization
   - View performance metrics in the stats box
   ```

4. **Compare Results**
   ```
   - Click "Clear Path" to keep the grid but remove the path
   - Try different algorithms on the same maze
   - Compare cells visited and path length
   ```

### Example Workflow

```bash
# 1. Open the application
open index.html

# 2. Set start point at top-left
#    (Click "Set Start" → Click cell [0,0])

# 3. Set end point at bottom-right
#    (Click "Set End" → Click cell [29,29])

# 4. Draw a vertical wall in the middle
#    (Click "Draw Walls" → Drag from top to bottom at column 15)

# 5. Run A* algorithm
#    (Click "A* Algorithm" button)

# 6. Clear and try Dijkstra
#    (Click "Clear Path" → Click "Dijkstra" button)

# 7. Compare results!
```

## 🧠 Algorithms

### 1. A* (A-Star) Algorithm

**Type**: Informed Search  
**Optimality**: Guaranteed  
**Complexity**: O(b^d) where b is branching factor, d is depth

**How it Works**:
- Uses f(n) = g(n) + h(n) cost function
- g(n): actual cost from start to node n
- h(n): Manhattan distance heuristic to goal
- Explores nodes with lowest f-score first

**Best For**:
- When optimal path is required
- Static environments with good heuristics
- Real-time applications needing efficiency

**Performance** (typical):
```
Cells Visited: 181
Path Length: 38 steps
Time: ~2200ms
Optimality: Yes ✓
```

### 2. Dijkstra's Algorithm

**Type**: Uninformed Search (Uniform Cost)  
**Optimality**: Guaranteed  
**Complexity**: O((V + E) log V)

**How it Works**:
- Explores uniformly in all directions
- Uses priority queue ordered by actual cost g(n)
- Guarantees shortest path in weighted graphs

**Best For**:
- When no good heuristic exists
- Finding shortest paths to multiple destinations
- Weighted graph scenarios

**Performance** (typical):
```
Cells Visited: 564
Path Length: 38 steps
Time: ~7500ms
Optimality: Yes ✓
```

### 3. Breadth-First Search (BFS)

**Type**: Uninformed Search  
**Optimality**: Guaranteed (unweighted graphs)  
**Complexity**: O(V + E)

**How it Works**:
- Explores layer by layer using FIFO queue
- Visits all nodes at distance d before d+1
- Wave-like expansion from start

**Best For**:
- Unweighted graphs
- Finding shortest path in simple grids
- Teaching fundamental search concepts

**Performance** (typical):
```
Cells Visited: 564
Path Length: 38 steps
Time: ~7100ms
Optimality: Yes ✓
```

### 4. Depth-First Search (DFS)

**Type**: Uninformed Search  
**Optimality**: Not guaranteed  
**Complexity**: O(V + E)

**How it Works**:
- Explores deeply along each branch using LIFO stack
- Backtracks when reaching dead ends
- May find longer paths

**Best For**:
- Memory-constrained scenarios
- Finding any path (not shortest)
- Exploring deep tree structures

**Performance** (typical):
```
Cells Visited: 137
Path Length: 110 steps
Time: ~1960ms
Optimality: No ✗
```

### 5. Q-Learning (Reinforcement Learning)

**Type**: Learning-Based  
**Optimality**: Near-optimal after training  
**Complexity**: O(episodes × max_steps)

**How it Works**:
- Learns Q-table through trial and error
- Q(s,a) = Q(s,a) + α[r + γ max Q(s',a') - Q(s,a)]
- α=0.1 (learning rate), γ=0.9 (discount factor)
- ε=0.3 (exploration rate)
- Trains for 500 episodes before execution

**Reward Structure**:
```python
+100  : Reaching the goal
-1    : Each step taken
+2×Δd : Moving closer to goal
```

**Best For**:
- Dynamic/changing environments
- Repeated navigation in same space
- Demonstrating adaptive learning

**Performance** (typical):
```
Cells Visited: 42
Path Length: 42 steps
Time: ~2950ms (includes training)
Optimality: Near (11% longer than optimal)
```

## 📊 Performance Comparison

### Benchmark Results
(30×30 grid, moderate complexity maze, optimal path = 38 steps)

| Algorithm   | Cells Visited | Path Length | Time (ms) | Optimal | Efficiency |
|-------------|---------------|-------------|-----------|---------|------------|
| A*          | 181           | 38          | 2,213.90  | ✅ Yes  | ⭐⭐⭐⭐⭐ |
| Dijkstra    | 564           | 38          | 7,459.90  | ✅ Yes  | ⭐⭐⭐     |
| BFS         | 564           | 38          | 7,140.60  | ✅ Yes  | ⭐⭐⭐     |
| DFS         | 137           | 110         | 1,962.70  | ❌ No   | ⭐⭐       |
| Q-Learning  | 42            | 42          | 2,951.50* | 🟡 Near | ⭐⭐⭐⭐   |

*Includes 500 episodes of training time

### Key Findings

1. **A* is the Winner**: 68% fewer cells visited than Dijkstra/BFS
2. **DFS Trades Quality for Speed**: Fastest execution but 189% longer path
3. **Q-Learning Learns Efficiency**: After training, visits only cells on path
4. **Dijkstra vs BFS**: Nearly identical in unweighted grids

## 🛠️ Technologies

- **HTML5**: Structure and Canvas API for grid rendering
- **CSS3**: Modern styling with gradients, animations, and transitions
- **JavaScript (ES6+)**: Algorithm implementations and interactivity
- **Google Fonts**: Poppins font family
- **No Dependencies**: Pure vanilla JavaScript, no frameworks needed!

## 📁 Project Structure

```
ai-pathfinding-visualizer/
├── index.html              # Main application file (standalone)
├── README.md               # This file
├── LICENSE                 # MIT License
├── research-paper/
│   ├── AI_Pathfinding_Research_Paper.docx
│   └── AI_Pathfinding_Research_Paper.pdf
├── screenshots/
│   ├── interface.png
│   ├── astar.png
│   ├── dijkstra.png
│   ├── bfs.png
│   ├── dfs.png
│   └── qlearning.png
└── docs/
    └── algorithm-details.md
```

## 📄 Research Paper

This project includes a comprehensive research paper in Springer conference format:

**Title**: *Interactive Web-Based Visualization of Pathfinding Algorithms: A Comparative Study*

**Abstract**: This research presents a comprehensive interactive web-based visualization system that enables direct comparison of five distinct pathfinding approaches. Through empirical analysis on identical maze configurations, we demonstrate that A* achieves optimal paths with 68% fewer cell explorations compared to uninformed search methods, while Q-Learning approaches near-optimal solutions through adaptive learning over 500 training episodes.

**Download**: [Research Paper (PDF)](research-paper/AI_Pathfinding_Research_Paper.pdf)

## 🎓 Educational Use

### For Students
- Visualize abstract algorithmic concepts
- Compare algorithm behavior in real-time
- Experiment with different maze configurations
- Understand trade-offs between algorithms

### For Educators
- Demonstrate pathfinding in lectures
- Create assignments with custom mazes
- Show reinforcement learning in action
- Interactive algorithm comparison tool

### Learning Outcomes
- Understanding of search algorithms
- Heuristic function design
- Graph traversal techniques
- Reinforcement learning basics
- Performance analysis skills

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

### Reporting Bugs

```bash
# Create an issue with:
- Description of the bug
- Steps to reproduce
- Expected vs actual behavior
- Screenshots (if applicable)
```

### Suggesting Enhancements

```bash
# Create an issue with:
- Feature description
- Use case/benefit
- Implementation suggestions
```

### Pull Requests

```bash
# Fork the repository
git clone https://github.com/yourusername/ai-pathfinding-visualizer.git

# Create your feature branch
git checkout -b feature/AmazingFeature

# Commit your changes
git commit -m 'Add some AmazingFeature'

# Push to the branch
git push origin feature/AmazingFeature

# Open a Pull Request
```

### Development Guidelines

1. **Code Style**: Follow existing code formatting
2. **Comments**: Add clear comments for complex logic
3. **Testing**: Test all algorithms with various maze configurations
4. **Documentation**: Update README if adding features

## 🔮 Future Enhancements

- [ ] Diagonal movement (8-connected grid)
- [ ] Weighted edges for Dijkstra demonstration
- [ ] Bidirectional search algorithms
- [ ] Jump Point Search (JPS)
- [ ] Dynamic obstacles that move during pathfinding
- [ ] Deep Q-Learning with neural networks
- [ ] Save/load maze configurations
- [ ] Algorithm speed control slider
- [ ] Maze generation algorithms
- [ ] 3D visualization mode
- [ ] Multi-agent pathfinding
- [ ] Mobile touch controls optimization
- [ ] Export results as CSV/JSON

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2025 Nazrana Nahreen

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## 👤 Author

**Nazrana Nahreen**

- 🎓 Department: Computer Science and Engineering
- 🏛️ Institution: International Islamic University Chittagong (IIUC)
- 📧 Email: c231444@ugrad.iiuc.ac.bd
- 💼 LinkedIn: [Your LinkedIn](https://linkedin.com/in/yourprofile)
- 🐱 GitHub: [@yourusername](https://github.com/yourusername)

## 🙏 Acknowledgments

- Inspired by classical AI pathfinding research
- Hart, P.E., Nilsson, N.J., Raphael, B. - A* Algorithm (1968)
- Dijkstra, E.W. - Shortest Path Algorithm (1959)
- Watkins, C.J., Dayan, P. - Q-Learning (1992)
- PathFinding.js visualization project
- International Islamic University Chittagong for academic support

## 📞 Support

If you found this project helpful:

⭐ **Star this repository**  
🐛 **Report bugs** via Issues  
💡 **Suggest features** via Issues  
🤝 **Contribute** via Pull Requests  
📧 **Contact** me directly for questions

## 📚 References

1. Hart, P.E., Nilsson, N.J., Raphael, B. (1968). A Formal Basis for the Heuristic Determination of Minimum Cost Paths. *IEEE Transactions on Systems Science and Cybernetics*, 4(2), 100-107.

2. Dijkstra, E.W. (1959). A Note on Two Problems in Connexion with Graphs. *Numerische Mathematik*, 1(1), 269-271.

3. Cormen, T.H., Leiserson, C.E., Rivest, R.L., Stein, C. (2009). *Introduction to Algorithms*, 3rd Edition. MIT Press.

4. Watkins, C.J., Dayan, P. (1992). Q-Learning. *Machine Learning*, 8(3-4), 279-292.

5. Russell, S.J., Norvig, P. (2020). *Artificial Intelligence: A Modern Approach*, 4th Edition. Pearson.

6. Sutton, R.S., Barto, A.G. (2018). *Reinforcement Learning: An Introduction*, 2nd Edition. MIT Press.

---

<div align="center">

### 🎯 Made with ❤️ for AI Education

**[View Demo](https://yourusername.github.io/ai-pathfinding-visualizer)** • 
**[Report Bug](https://github.com/yourusername/ai-pathfinding-visualizer/issues)** • 
**[Request Feature](https://github.com/yourusername/ai-pathfinding-visualizer/issues)**

</div>

---

<div align="center">

**Happy Pathfinding! 🚀**

If you found this project helpful, please consider giving it a ⭐

</div>
