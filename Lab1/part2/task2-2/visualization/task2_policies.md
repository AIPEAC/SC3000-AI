# Task 2: Monte Carlo Learning

## Problem
5x5 Grid World with stochastic transitions. Unknown environment model.
Stochastic transitions: 0.8 intended, 0.1 each perpendicular direction.
Epsilon-greedy exploration with epsilon=0.1.

## Learned Policy

## Monte Carlo - Learned Policy

| X\Y | 0 | 1 | 2 | 3 | 4 |
|-----|---|---|---|---|----|
| 4 | DOWN | RIGHT | RIGHT | RIGHT | GOAL |
| 3 | RIGHT | RIGHT | RIGHT | RIGHT | UP |
| 2 | UP | OBS | UP | OBS | UP |
| 1 | RIGHT | RIGHT | UP | RIGHT | UP |
| 0 | RIGHT | RIGHT | RIGHT | RIGHT | UP |

## Legend
- `UP` = Move up
- `DOWN` = Move down
- `LEFT` = Move left
- `RIGHT` = Move right
- `OBS` = Obstacle
- `GOAL` = Goal state (4,4)

## Similarity with Optimal Policy

- **Reference**: Value Iteration optimal policy (Task 2-1)
- **Evaluated states**: 22 (excludes obstacles and goal)
- **Matches**: 18 / 22
- **Similarity**: **81.8%**
- **Mismatched states**:
  - (0,0) learned RIGHT, optimal UP
  - (0,2) learned RIGHT, optimal UP
  - (1,0) learned RIGHT, optimal UP
  - (4,0) learned DOWN, optimal RIGHT

