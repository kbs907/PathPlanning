
# RRT
> ## Goal
> 
> ![](https://github.com/kbs907/PathPlanning/blob/main/RRT/pseudo_RRT.png?raw=true)
> 
> 논문의 pseudo code를 이용하여 직접 구현하고, 성능향상을 위해 heuristic algorithm 추가
> 
> </br></br>
> 
> ## Result
> ### 랜덤으로 탐색했을 경우
> ![](https://github.com/kbs907/PathPlanning/blob/main/RRT/rrt_random_100.png?raw=true)
> 
> </br>
> 
> ### 90% 확률로 랜덤한 지점 선택, 10% 확률로 목표지점 선택
> ![](https://github.com/kbs907/PathPlanning/blob/main/RRT/rrt_random_90.png?raw=true)
> 
> heuristic을 적용했을 때 좀더 빠르게 목표지점에 도달하는 것을 확인
 
</br></br>
 
 # RRT*
 > ## Goal
 >
 >![](https://github.com/kbs907/PathPlanning/blob/main/RRT_STAR/pseudo_RRT*.png?raw=true)
 >
 > 논문의 pseudo code를 이용하여 직접 구현하고, 성능향상을 위해 heuristic algorithm 추가
 >
 > </br></br>
 >
 > ## Result (RRT와 RRT* 비교)
 > ### RRT의 경우
 > ![](https://github.com/kbs907/PathPlanning/blob/main/RRT_STAR/rrt.png?raw=true)
 >
 > </br>
 >
 > ### RRT*의 경우
 > ![](https://github.com/kbs907/PathPlanning/blob/main/RRT_STAR/rrt_star.png?raw=true)
 >
 > 기존 RRT와 다르게, 탐색한 노드중에서 cost를 낮출 수 있는 경우 rewiring을 하여 좀더 최적의 경로를 생성하는것을 확인

</br></br>

 # Dubins Path
 > ## Goal
 >
 > 논문의 식을 이용하여 6가지 경로 생성하는 코드를 직접 구현하고 동작 확인
 >
 > </br></br>
 >
 > ## Result (6가지 경로 확인)
 > ### 6가지 경로
 > ![](https://github.com/kbs907/PathPlanning/blob/main/Dubins/Dubins.png?raw=true)
 >
 > </br>
 > 
 > ### LRL
 > ![](https://github.com/kbs907/PathPlanning/blob/main/Dubins/Dubins_LRL.png?raw=true)
 >
 > </br>
 >
 > ### LSL
 > ![](https://github.com/kbs907/PathPlanning/blob/main/Dubins/Dubins_LSL.png?raw=true)
 >
 > </br>
 > 
 > ### LSR
 > ![](https://github.com/kbs907/PathPlanning/blob/main/Dubins/Dubins_LSR.png?raw=true)
 >
 > </br>
 > 
 > ### RLR
 > ![](https://github.com/kbs907/PathPlanning/blob/main/Dubins/Dubins_RLR.png?raw=true)
 >
 > </br>
 > 
 > ### RSL
 > ![](https://github.com/kbs907/PathPlanning/blob/main/Dubins/Dubins_RSL.png?raw=true)
 >
 > </br>
 > 
 > ### RSR
 > ![](https://github.com/kbs907/PathPlanning/blob/main/Dubins/Dubins_RSR.png?raw=true)
 >
 > </br></br>

# RRT & Dubins
 > ## Goal
 >
 > RRT는 충돌 확인을 하며 경로 탐색을 하지만, 무작위의 discrete한 지점을 탐색하기에 차량이 이동할 수 없는 경로를 생성하는 단점이 있다.</br>
 > Dubins는 차량이 회전할 수 있는 curvature를 고려하여 경로를 생성하지만 충돌 확인을 하며 경로 탐색을 하지 못한다.
 >
 > 각 단점들을 상호 보완하기 위해 이전에 구현한 RRT 코드에서 각 노드를 이을때 Dubins경로로 잇도록 직접 구현
 >   
 > </br></br>
 >
 > ## Result
 > ![](https://github.com/kbs907/PathPlanning/blob/main/RRT_Dubins/rrt_dubins.png?raw=true)
 >
 >
 > rrt처럼 탐색을 하되, 의도한대로 각 노드간 경로가 Dubins path인 것을 확인할 수 있다

