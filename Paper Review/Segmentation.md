# Object Segmentation in 3D / Indoor

### (1) Segmentation of Unknown Objects in Indoor Environments

Overview : Fig2
Plane Fitting과 NURBS Fitting을 활용하여 각각 Plane인 부분과 Curvature부분으로 나누어 Fitting후 SVM을 이용하여 클러스터링 함
여기서 활용하는 Feature가 무지 다양하여 SVM으로 Feature를 갈라내는 parameter를 학습시켜, 이걸 Same Cluster로 볼지 아닐지를 학습

What is input for SVM?
 $r_{nb}$ and $r_{nnb}$ which means neighbouring and non neighbouring vector
 SVM can devide $r_{nb}$ and $r_{nnb}$

 아직 이해가 부족하다. 다시 읽어보자

어쨌든 이걸로 Segmentation한 거는 Unknown이여도 꽤 잘되고, Known이 섞여 있으면 더 쉽고 Pose estimation까지 되겠지.
