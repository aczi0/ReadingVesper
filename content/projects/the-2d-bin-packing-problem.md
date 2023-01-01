+++
date = 2023-01-01T05:00:00Z
title = "The 2D Bin Packing Problem"

+++
**2D bin packing** is a type of optimization problem that involves fitting a set of 2D rectangles (also known as "items") into a single, larger rectangle (also known as the "bin") in such a way that the items are arranged as efficiently as possible. It is used in a variety of applications, including:

* **Packaging**: 2D bin packing can be used to determine the most efficient way to pack a set of items into a container for shipping or storage.
* **Scheduling**: In manufacturing and other industries, 2D bin packing can be used to schedule the use of resources such as machine time or floor space.
* **Data compression**: 2D bin packing can be used to compress data by finding an efficient way to arrange the data in a fixed-size block.
* **Layout design**: 2D bin packing can be used to design efficient layouts for warehouses, factories, and other types of buildings.
* **Graph drawing**: In graph theory, 2D bin packing can be used to layout the nodes and edges of a graph in a way that minimizes the amount of space required.

An example of a 2D Bin Packing problem that tries to fit 5 rectangles (10x15, 20x25, 30x35, 40x45, 50x55) inside a larger rectangle (bin size of 100x200).

    from ortools.linear_solver import pywraplp
    
    def main():
      # Set the size of the bin and the sizes of the items.
      bin_width = 100
      bin_height = 200
      width = [10, 20, 30, 40, 50]
      height = [15, 25, 35, 45, 55]
      n = len(width)
    
      # Create the solver.
      solver = pywraplp.Solver('2D Bin Packing', pywraplp.Solver.GLOP_LINEAR_PROGRAMMING)
    
      # Create the variables.
      x = {}
      y = {}
      for i in range(n):
        x[i] = solver.NumVar(0, solver.infinity(), 'x[%i]' % i)
        y[i] = solver.NumVar(0, solver.infinity(), 'y[%i]' % i)
    
      # Set the objective function.
      objective = solver.Minimize(max(x) + max(y))
    
      # Set the constraints.
      for i in range(n):
        solver.Add(x[i] + width[i] <= bin_width)
        solver.Add(y[i] + height[i] <= bin_height)
    
      # Solve the problem.
      status = solver.Solve()
    
      # Print the solution.
      if status == pywraplp.Solver.OPTIMAL:
        print('Optimal solution found.')
        for i in range(n):
          print('Item', i, ':', 'x =', x[i].solution_value(), 'y =', y[i].solution_value())
      else:
        print('Problem could not be solved.')
    
    if __name__ == '__main__':
      main()