# DOSP_Project2



## Team Members:
Uma Sai Sree Avula - UFID : 38554667<br/>
Bhanu Rekha Musuluri - UFID : 98477459<br/>

## Description
This project implements the gossip algorithm which is used for propagation of the data. There are actors in the model and each actor stores two variables s and w. Upon receiving the message from other neighbour actors, the variables get added up and upon sending the messages the values of variables are halved. Each time s/w value is calculated and we terminate the algorithm when the value of s/w doesn't change more than 10^-10 in 3 consecutive rounds. Hence this project is helpful in determining the convergence of gossip algorithm.   

## Execution Steps - 

1. Create a node for the server using the command -

      erl -name uavula@192.168.0.105

2. Compile the modules using the command -

      c(gossip). <br/>
      c(pushsum). <br/>
      c(topology). <br/>
      c(main). <br/>

3. To start the compiled program and enable the main module, use the command - 

      main:start(8192, "2D", "gossip").

      Here the first argument represents the number of workers. The second argument represents the type of topology. The third argument represents the name       of the algorithm.


## Report Questions

1. What is working ? -

    This project works for 2D Grid, Full Network, Line, Imperfect 3D Grid.

2. What is the largest network you managed to deal with for each type of topology and algorithm ?

      | Algorithm | Topology | Network | Amount of time to converge |
      | --------- | -------- | ------- | -------------------------- |
      | Gossip    | Line     | 4096    | 598476                     |
      | Gossip    | Full     | 16384   | 21785                      |
      | Gossip    | 2D       | 8192    | 15025                      |
      | Gossip    | Imp 2D   | 16384   | 3230                       |
      | PushSum   | Line     | 4096    | 173487                     |
      | PushSum   | Full     | 8192    | 10002                      |
      | PushSum   | 2D       | 8192    | 144905                     |
      | PushSum   | Imp 2D   | 32768   | 7611                       |
       

Line Topology for Gossip Algorithm
<img width="864" alt="gossipLine" src="https://user-images.githubusercontent.com/57837608/194991595-26ee7bff-77a5-4692-8658-003f2bfe9f72.png">

Full Network Topology for Gossip Algorithm
<img width="889" alt="GossipFull" src="https://user-images.githubusercontent.com/57837608/194991610-1451884d-37f3-476a-9598-83b7e4b4de26.png">

2D Topology for Gossip Algorithm
<img width="780" alt="gossip2D" src="https://user-images.githubusercontent.com/57837608/194991624-f114a448-d2ca-4b11-8bb1-4a484a292bc2.png">


Imp 3D for Gossip Algorithm <br/>
<img width="714" alt="gossipImp2D" src="https://user-images.githubusercontent.com/57837608/194991637-3d1d112a-b00b-4416-a1b5-9548da331e00.png">

Line Topology for PushSum Algorithm
<img width="841" alt="PushSumLine" src="https://user-images.githubusercontent.com/57837608/194991654-92bc3094-e5ea-4096-ac1b-0f27c5cbbf32.png">

Full Network Topology for PushSum Algorithm
<img width="769" alt="PushSumFull" src="https://user-images.githubusercontent.com/57837608/194991662-57900572-4a82-4b64-86f5-1927977483ab.png">

2D Topology for PushSum Algorithm
<img width="775" alt="PushSum2D" src="https://user-images.githubusercontent.com/57837608/194991669-0f10896c-c28f-4e2c-91c0-e7d6f0c6c143.png">

Imp 3D Topology for PushSum Algorithm
<img width="844" alt="PushSumImp2D" src="https://user-images.githubusercontent.com/57837608/194991679-cd2f5509-11e9-4e85-b877-36e3354c7b9d.png">


 
 





 




