# Simulation
Computer Simulation Final Project
Matt Doherty, Nicholas Fong, Julia Marcondes, Christina Matera

Factory Project:
     - 7 different machines running at the same time
     - Machines come in two varieties: one is very fast but it breaks down and it’s more expensive to repair, the other is slower but more reliable and is cheaper 
     - Find best combinations of slow/fast machines
     - We will get the beta distributions later


Project Description:
    A factory holds 7 machines, each of which can be one of two varieties of machine.The first variety is a machine with a high throughput and quick production speed, but also more likely to break down and be out of service. When this first machine type breaks down, it is slow to repair, so it is out of commission for a long time. The second variety is a machine with a low throughput and slow production speed, but also less likely to break down and be out of service. When this second machine type breaks down, it is quick to repair, so it is only out of commission for a short period of time.
    There is only one repair crew for each class of machine; only one machine of each class can be repaired at a time.
    We will run a simulation to predict the most efficient combination of the first and second varieties in our factory of seven machines. We will run this simulation over a long period of time and will be able to report the frequency of extreme events (ex. three days out of year, all systems down), and also the overall rate of production for each combination of machines.


We need:
    State variables
    Counter variables
    Search strategy 
    Event list

State Variables:
    Broken/Working state of all 7 machines
    Rate of production for each machine
    Number of fast machines / slow machines


Counter Variables:
    Total products made
    Total wait time for repairing machines
    Cost of repairs
    End of period profit (total products made - cost of repair)
    Time spent fixing each machine


Event List:
    A machine breaks down
    A machine is repaired
    A product is made


Search Strategy:
    Perform many trials each combination of n fast machines and (7-n) slow machines with  0 <= n <= 7, averaging the results to find the combination that optimizes profit, by taking into account:
            Cost of repairs
            Revenue from products (just a function of how many products are made)
            Machine down time (Only indirectly affects profits so this might not be needed, but it might be relevant if we want a more consistent factory)
