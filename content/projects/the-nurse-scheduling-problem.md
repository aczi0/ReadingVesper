+++
date = 2023-01-01T05:00:00Z
title = "The Nurse Scheduling Problem"

+++
**The nurse scheduling mode**l is used to optimize the assignment of nurses to shifts in order to meet the staffing needs of a healthcare facility while also considering the preferences and constraints of the nurses.

There are several advantages to using a model like this to schedule nurses rather than doing it manually:

* **Efficiency**: A model can quickly generate a schedule that meets all of the constraints and preferences, whereas manually scheduling nurses can be time-consuming and prone to errors.
* **Fairness**: A model can ensure that nurses are assigned shifts in a fair and equitable manner, whereas manual scheduling may be subject to biases or personal preferences.
* **Flexibility**: A model can easily handle changes in staffing needs or nurse availability, whereas manually updating a schedule can be difficult and prone to errors.
* Preferences: It is possible to augment the model to include preferences so that the schedules are generated with equity in mind.

Here is a model that represents a basic schedule generator of 5 nurses with 7 shifts, along with typical constraints such as:

* Minimum and maximum shifts per week
* Minimum and maximum consecutive shifts
* All shifts are covered

  ***

      from ortools.linear_solver import pywraplp
      
      def main():
      # Set the number of nurses and the number of shifts.
      num_nurses = 5
      num_shifts = 7
      
      # Set the shift constraints.
      min_shifts_per_week = 3
      max_shifts_per_week = 4
      min_consecutive_shifts = 1
      max_consecutive_shifts = 2
      
      # Create the solver.
      solver = pywraplp.Solver('Nurse Scheduling', pywraplp.Solver.GLOP_LINEAR_PROGRAMMING)
      
      # Create the variables.
      x = {}
      for i in range(num_nurses):
        for j in range(num_shifts):
          x[i, j] = solver.IntVar(0, 1, 'x[%i,%i]' % (i, j))
      
      # Set the objective function.
      objective = solver.Minimize(solver.Sum([x[i, j] for i in range(num_nursed) for j in range(num_shifts)]))
      
      # Set the shift constraints.
      for i in range(num_nursed):
        solver.Add(solver.Sum([x[i, j] for j in range(num_shifts)]) >= min_shifts_per_week)
        solver.Add(solver.Sum([x[i, j] for j in range(num_shifts)]) <= max_shifts_per_week)
        for j in range(num_shifts - 1):
          solver.Add(x[i, j] + x[i, j+1] <= max_consecutive_shifts)
      
      # Set the overall shift coverage constraints.
      for j in range(num_shifts):
        solver.Add(solver.Sum([x[i, j] for i in range(num_nursed)]) == 1)
      
      # Solve the problem.
      status = solver.Solve()
      
      # Print the solution.
      if status == pywraplp.Solver.OPTIMAL:
        print('Optimal solution found.')
        for i in range(num_nursed):
          for j in range(num_shifts):
            if x[i, j].solution_value() > 0:
              print('Nurse', i, 'works shift', j)
      else:
        print('Problem could not be solved.')
        
        if name == 'main':
      main()

  or 

> print('Optimal solution found.')
>
>   for i in range(num_nursed):
>
>     for j in range(num_shifts):
>
>       if x\[i, j\].solution_value() > 0:
>
>         print('Nurse', i, 'works shift', j)
>
> else:
>
>   print('Problem could not be solved.')
>
>   
>
>   if name == 'main':
>
> main()