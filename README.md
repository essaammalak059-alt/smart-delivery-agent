# Smart Delivery Agent Using A* Search Algorithm

## 1. Project Idea
The Smart Delivery Agent is an AI project that finds the best delivery route from a Warehouse to a Customer.

The system uses the A* Search Algorithm to find the path with the lowest total cost. It can also handle blocked roads and find alternative routes.

## 2. Team Members

| Name | Student ID |
|---|---|
| Malak Essam | 24030162 |
| Haneen Ibrahim | 24030152 |
| Omnia Mohamed | 24030099 |

## 3. Course Information

- University: Innovation University
- Faculty: Faculty of Computers and Information Technology
- Course: Fundamentals of AI
- Course Code: CF321
- Project: Project 1

## 4. Algorithm Used

We used the A* Search Algorithm.

A* uses the following evaluation function:

f(n) = g(n) + h(n)

- g(n): Actual cost from the start node.
- h(n): Estimated cost to the goal.
- f(n): Total estimated cost.

We chose A* because it considers both the actual path cost and the estimated remaining cost.

## 5. Problem Definition

- States: Warehouse, A, B, C, Customer.
- Initial State: Warehouse.
- Goal State: Customer.
- Available Actions: Moving between connected locations.
- Action Cost: The cost of traveling between two locations.

## 6. Heuristic Function

The heuristic values are:

| Location | Heuristic |
|---|---:|
| Warehouse | 7 |
| A | 4 |
| B | 6 |
| C | 3 |
| Customer | 0 |

These values estimate the remaining cost to reach the Customer.

## 7. Implementation

The project was implemented using Python in Google Colab.

Libraries used:
- NetworkX
- Matplotlib

The implementation includes:
- Road map representation.
- A* search implementation.
- Blocked road handling.
- Path cost calculation.
- Nodes explored counting.
- Road map visualization.

## 8. Testing and Results

### Test 1: Normal Test
Best Route:
Warehouse → B → C → Customer

Total Delivery Cost: 9

Nodes Explored: 5

### Test 2: Closed Road Test
The road between B and C is blocked.

Alternative Route:
Warehouse → A → C → Customer

Total Delivery Cost: 13

Nodes Explored: 5

### Test 3: No Route Test
No available route to the customer.

Nodes Explored: 4

## 9. How to Run the Project

1. Open the project notebook in Google Colab.
2. Run all cells in order.
3. Observe the results of the three test cases.
4. View the route visualization.

## 10. Conclusion

The project demonstrates how the A* Search Algorithm can solve a delivery route-planning problem.

The agent can find the lowest-cost route, handle blocked roads, and detect when no available route exists.
