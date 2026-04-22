# A Workload-Adaptive Multi-Heuristic System for Delivery Route Optimization

## This project presents a workload-adaptive delivery route optimization system designed to improve efficiency, fairness, and stability in multi-agent logistics environments.
Unlike traditional routing systems that focus only on minimizing distance or cost, this system integrates workload balancing directly into the optimization process, ensuring equitable task distribution among delivery agents while maintaining high routing efficiency

## Key Objectives
* Minimize total travel distance and operational cost
* Ensure balanced workload distribution across delivery agents
* Reduce agent fatigue through historical workload tracking
* Prevent repetitive or biased task allocation
* Maintain stability and fairness in dynamic environments


## Core Features

**1. Workload-Aware Optimization**
* Computes workload for each agent based on route distance
* Uses workload variance to measure imbalance
* Penalizes uneven task distribution during optimization

**2. Fairness Control Mechanism**
* Integrates fairness directly into the fitness function
* Ensures no agent is consistently overloaded or underutilized

**3. Adaptive Control Strategy**
* Dynamically adjusts optimization behavior based on:
  * Workload imbalance
  * System convergence
* Promotes redistribution when imbalance is high
* Refines solutions when the system is stable

**4. Fatigue-Aware Allocation**
* Tracks cumulative workload across iterations
* Applies penalties to prevent repeated overloading of agents
* Improves long-term system stability

**5. Novelty-Based Search**
* Compares current workload patterns with previous ones
* Encourages diverse routing solutions
* Prevents premature convergence

**6. Multi-Heuristic Optimization**
* Combines global search with local route improvement (2-opt)
* Enhances solution quality and convergence speed


##  Methodology

**Step-by-Step Workflow**
1. Initialize population of routing solutions
2. Decode routes into delivery-agent assignments
3. Compute workload for each agent
4. Calculate workload variance (fairness metric)
5. Evaluate novelty of workload distribution
6. Apply fatigue penalty using historical workload
7. Adapt control parameters dynamically
8. Compute final fitness value
9. Perform selection, crossover, and mutation
10. Repeat until convergence
11. Output optimized routing solution

## Fitness Function
The system evaluates each solution using a composite fitness function that balances:
* Total route distance
* Workload variance (fairness)
* Maximum workload
* Total workload
* Fairness index
* Fatigue penalty
* Task distribution balance

## Experimental Validation
The system demonstrates significant improvement in workload balancing:
* Initial workload variance: High imbalance
* Optimized workload variance: Significantly reduced
* Improved fairness and agent utilization
* Stable convergence across iterations
* Efficient and structured routing performance


## Outputs
The project generates:
* **Fitness improvement over 60 generations**
    Shows percentage improvement in solution quality across evolutionary iterations
* **Optimized delivery routes visualization**
    Displays agent-wise routing after optimization
* **Baseline route comparison**
    Compares workload-adaptive routing with round-robin baseline (Dijkstra-style) allocation
* **Performance Metrics Comparison**
   * Total distance
   * Maximum workload
   * Workload variance
   * Fairness index


## How to Run

```bash
pip install -r requirements.txt
python main.py
```


## Project Structure

```
.
├── main.py
├── README.md
├── requirements.txt
├── outputs/
│   ├── fitness_convergence.png
│   ├── optimized_routes.png
│   └── comparison.png
```


## Future Scope
* Integration with real-time traffic data
* Dynamic delivery request handling
* Machine learning-based parameter tuning
* Web-based visualization dashboard
* Scalable deployment for large logistics networks


##  Contribution
This project introduces a unified framework where workload balancing is not a post-processing step but an integral part of the optimization process, enabling fair, adaptive, and efficient delivery routing.
