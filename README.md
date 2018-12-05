# Astar-Algorithm-in-Puzzle8
A* (A-star) algorithm is one of the most effective direct search methods for solving shortest path in Static road network, and it is also a common heuristic algorithm for many other problems.

![Puzzle8 with A*Algorithm.png](https://github.com/zouhao0418/Astar-Algorithm-in-Puzzle8/blob/master/Puzzle8%20with%20A*Algorithm.png)

```
frontier = PriorityQueue() frontier.put(start, 0)
     came_from = {}
     cost_so_far = {}
     came_from[start] = None
     cost_so_far[start] = 0
     while not frontier.empty():
        current = frontier.get()
        if current == goal:
           break
        for next in graph.neighbors(current):
           new_cost = cost_so_far[current]+graph.cost(current,
next)
           if next not in cost_so_far or new_cost <
cost_so_far[next]:
              cost_so_far[next] = new_cost
              priority = new_cost + heuristic(goal, next)
              frontier.put(next, priority)
              came_from[next] = current
```
