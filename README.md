# Single server with infinite capacity (M/M/1):(oo/FIFO)
## Aim :
To find (a) average number of materials in the system (b) average number of materials in the conveyor (c) waiting time of each material in the system (d) waiting time of each material in the conveyor, if the arrival  of materials follow poisson process with the mean interval time 12 seconds, serivice time of lathe machine follows exponential distribution with mean serice time 1 second and average service time of robot is 7seconds.

## Software required :
Visual components and Python

## Theory:
Queuing are the most frequently encountered problems in everyday life. For example, queue at a cafeteria, library, bank, etc. Common to all of these cases are the arrivals of objects requiring service and the attendant delays when the service mechanism is busy. Waiting lines cannot be eliminated completely, but suitable techniques can be used to reduce the waiting time of an object in the system. A long waiting line may result in loss of customers to an organization. Waiting time can be reduced by providing additional service facilities, but it may result in an increase in the idle time of the service mechanism.

![image](1.png)

This is a queuing model in which the arrival is Marcovian and departure distribution is also Marcovian,number of server is one and size of the queue is also Marcovian,no.of server is one and size of the queue is infinite and service discipline is 1st come 1st serve(FCFS) and the calling source is also finite.

## Procedure :

![imAGE](2.png)


## Experiment:

![321572044-bc252606-8a2f-479a-8178-f5c9ad1afb92](https://github.com/user-attachments/assets/cb648ada-9aba-4c46-b4d4-3b6a1e4236cd)

 
## Program
```
Developed By: RAVIPRASATH K
Register No: 212224230225

arr_time=float(input("Enter the mean inter arrival time of objects from Feeder (in secs): "))
ser_time=float(input("Enter the mean  inter service time of Lathe Machine (in secs) :  "))
Robot_time=float(input("Enter the Additional time taken for the Robot (in secs) :  "))
lam=1/arr_time
mu=1/(ser_time+Robot_time)
print("--------------------------------------------------------------")
print("Single Server with Infinite Capacity - (M/M/1):(oo/FIFO)")
print("--------------------------------------------------------------")
print(f"The mean arrival rate per second : {lam:.2f}")
print(f"The mean service rate per second : {mu:.2f}")
if (lam <  mu):
    Ls=lam/(mu-lam)
    Lq=Ls-lam/mu
    Ws=Ls/lam
    Wq=Lq/lam
    print(f"Average number of objects in the system : {Ls:.2f}")
    print(f"Average number of objects in the conveyor :  {Lq:.2f}")
    print(f"Average waiting time of an object in the system : {Ws:.2f} secs")
    print(f"Average waiting time of an object in the conveyor : {Wq:.2f} secs")
    print(f"Probability that the system is busy : {(lam/mu):.2f}" )
    print(f"Probability that the system is empty : {(1-lam/mu):.2f}" )
else:
    print("Warning! Objects Over flow will happen in the conveyor")
print("---------------------------------------------------------------")
```

## Output :

![image](https://github.com/user-attachments/assets/14fd14fd-a968-40b2-aee3-77d8efefcb10)

## Result :

The average number of material in the sysytem and in the conveyor and waiting time are successfully found.

