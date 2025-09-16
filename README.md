# POLICY ITERATION ALGORITHM

## AIM
To develop a Python program to find the optimal policy for the given MDP using the policy iteration algorithm.

## PROBLEM STATEMENT
The aim of this experiment is to find optimal policy for the mdp using policy iteration. Policy iteration includes policy evaluation and policy improvement where evaluation function is used to find optimal value function of each state and then improvement function is used to find best policy by comparing all the action value function as well as policy.

## POLICY ITERATION ALGORITHM
-> Step1 :
We are going to do policy evaluation of each state to get the state value function where the initial policy is defined randomly to the mdp.

-> Step2:
Once we obtain convergence in the policy evaluation then implement policy improvement where we are going to find best optimal policy until the previous and current policy are same.
</br>
</br>

## POLICY IMPROVEMENT FUNCTION
#### Name : SAKTHIVEL M
#### Register Number : 212222240088
```python
def policy_improvement(V, P, gamma=1.0):
    Q = np.zeros((len(P), len(P[0])), dtype=np.float64)
    # Write your code here to improve the given policy
    for s in range(len(P)):
      for a in range(len(P[s])):
        for prob,next_state,reward,done in P[s][a]:
          Q[s][a]+=prob*(reward+gamma*V[next_state]*(not done))
          new_pi=lambda s:{s:a for s, a in enumerate(np.argmax(Q,axis=1))}[s]
    return new_pi
```
## POLICY ITERATION FUNCTION
#### Name : SAKTHIVEL M
#### Register Number : 212222240088
```python
def policy_iteration(P, gamma=1.0, theta=1e-10):
   random_actions=np.random.choice(tuple(P[0].keys()),len(P))
   pi = lambda s: {s:a for s, a in enumerate(random_actions)}[s]
   while True:
    old_pi = {s:pi(s) for s in range(len(P))}
    V = policy_evaluation(pi, P,gamma,theta)
    pi = policy_improvement(V,P,gamma)
    if old_pi == {s:pi(s) for s in range(len(P))}:
      break
   return V, pi
```

## OUTPUT:
### 1. Policy, Value function and success rate for the Adversarial Policy
<img width="588" height="163" alt="Screenshot 2025-09-16 205613" src="https://github.com/user-attachments/assets/4f42c504-1eed-4fd4-8251-3b10bc91c145" />
<img width="751" height="42" alt="Screenshot 2025-09-16 205639" src="https://github.com/user-attachments/assets/7a6628e3-9ed4-4caf-9802-9cb90b78dd1f" />
<img width="547" height="169" alt="Screenshot 2025-09-16 205959" src="https://github.com/user-attachments/assets/23f8d591-06fc-433c-b871-68818a8d4691" />


### 2. Policy, Value function and success rate for the Improved Policy
<img width="563" height="172" alt="Screenshot 2025-09-16 211749" src="https://github.com/user-attachments/assets/04651147-2a01-4a6d-9422-c6ecf250802d" />
<img width="708" height="45" alt="Screenshot 2025-09-16 211807" src="https://github.com/user-attachments/assets/096de9f0-9e13-4a30-af9a-63c9e8855297" />
<img width="574" height="180" alt="Screenshot 2025-09-16 211820" src="https://github.com/user-attachments/assets/f04c30e2-c482-403f-b850-c4185df5ba2d" />


### 3. Policy, Value function and success rate after policy iteration
<img width="702" height="200" alt="Screenshot 2025-09-16 212648" src="https://github.com/user-attachments/assets/014e686b-86fb-45ba-83ad-49dca1fa70db" />
<img width="724" height="47" alt="Screenshot 2025-09-16 212703" src="https://github.com/user-attachments/assets/feaec0e4-dcd5-4881-8c0d-c532abd37207" />
<img width="889" height="150" alt="Screenshot 2025-09-16 212720" src="https://github.com/user-attachments/assets/836301eb-5c3d-4a25-a19d-fa8caf4c95f0" />




## RESULT:
Thus, The Python program to find the optimal policy for the given MDP using the policy iteration algorithm is successfully executed.
