# Optimization-of-Maintenance-Scheduling-for-Generators-using-ILP

This work optimizes the maintenance schedule for a set of generators in a power network using integer linear programming (ILP).

It is assumed that the power plant has 10 generators:
- 6 300 MW generators 
- 4 100 MW generators 

It is also assumed that the duration of maintenance for each type of generators is as follows:
- 3 weeks for 300 MW generators
- 2 weeks for 100 MW generators 

There are 3 maintenance teams available. This means that at most 3 generators can be under maintenance at a given time. 

The duration of study is 12 weeks. The load peak demand varies over the course of these 12 weeks as shown in the workbook "Demand.xlsx". 

This work takes a reserve-based approach. When choosing which units are to be put under maintenance in a certain week, it is not enough to ensure that the entire load demand is met (achieved through making sure that the generation exceeds the demand). It is also important to maintain a certain reserve margin. 

If all units are to be put under maintanence, the total sum of reserve over the 12 weeks will be the same regardless of the maintenance schedule. However, it may be very low under some weeks and excessively high in other weeks. Hence, it is important to keep this reserve steady over all 12 weeks. Please refer to "Reserve.png" for an illusration of this idea. 

In other words, we want the reserve values over each week to be very close to each other. This can be achieved by minimizing an L1 norm. Naturally, such an optimization problem can be linearized. 

### Note: The code exists in ".mlx" and ".m" forms. 
#### The ".mlx" version is suggested for better interpretability. 
