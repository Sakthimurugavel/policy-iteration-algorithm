# POLICY ITERATION ALGORITHM

## AIM
The aim of this experiment is to implement the **Policy Iteration Algorithm** in Reinforcement Learning to determine the optimal policy and corresponding value function for a given environment. Policy Iteration combines iterative **policy evaluation** and **policy improvement** steps to achieve convergence towards an optimal policy.

## PROBLEM STATEMENT
In Reinforcement Learning, the agent interacts with an environment modeled as a Markov Decision Process (MDP).  
The challenge is to find an **optimal policy** that maximizes the long-term cumulative reward.  
Policy Iteration addresses this by:
1. Evaluating the value of a given policy (Policy Evaluation).
2. Improving the policy based on the evaluated value function (Policy Improvement).
3. Repeating these steps until the policy converges to the optimal policy.

## POLICY ITERATION ALGORITHM
The steps involved in the **Policy Iteration Algorithm** are:

1. **Initialization**  
   - Initialize an arbitrary policy π and value function V(s).

2. **Policy Evaluation**  
   - For the current policy π, compute the value function V(s) for all states until convergence.

3. **Policy Improvement**  
   - Update the policy by choosing actions that maximize the expected return using the current value function.

4. **Check for Convergence**  
   - If the policy does not change (π′ = π), then the policy is optimal and the algorithm terminates.
   - Otherwise, repeat steps 2 and 3.

## POLICY IMPROVEMENT FUNCTION
### Name :
### Register Number
```python
Include the policy improvement function







```
## POLICY ITERATION FUNCTION
### Name
### Register Number
```python
Include the policy iteration function






```

## OUTPUT:
### 1. Policy, Value function and success rate for the Adversarial Policy
</br>
</br>

### 2. Policy, Value function and success rate for the Improved Policy
</br>
</br>

### 3. Policy, Value function and success rate after policy iteration
</br>
</br>


## RESULT:

Write your result here
