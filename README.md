# os_project

___

To implement the above problem we have to take the Banker’s Algorithm, which is a deadlock avoidance algorithm. It is called the Banker’s Algorithm. When a new process enters the system, it declares the maximum number of instances that are needed. This number cannot exceed the total number of resources in the system.  If the process can be accommodated based upon the needs of the system, then resources are allocated, otherwise the process must wait.

Step 1: Let Work and Finish be vectors of length ‘m’ and ‘n’ respectively.
   Initialize: Work = Available
   Finish[i] = false; for (i=1, 2, 3, 4….n)

Step 2: Find an i such that both
   Finish[i] = false
   Needi <= Work
   if no such i exists goto step (4)

Step 3: Work = Work + Allocation[i]
   Finish[i] = true
   Goto step (2)

Step4: if Finish [i] = true for all i
   Then the system is in a safe state