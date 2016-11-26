
### Delft Amazon Team Delft’s Robot Winner of the Amazon Picking Challenge 2016

- Task Management
  - Whole tasks are managed by **ROS SMACH** as a state machine.
  - It encodes the competition rules to maximize the scoring.

- Object Recognition : Faster R-CNN using RGB, 150ms
  - 이것을 위해 20,000 Base image제작 - 다양한 방향, 배경으로다가,

- Pose Estimation : Super 4PCS -- match the filtered Point Cloud of the target item with a CAD model of the object.
  - Mellado, N., Aiger, D., Mitra, N.J.: Super 4pcs fast global pointcloud registration via smart indexing. Computer Graphics Forum 33(5) (2014) 205–215
  -> Pose estimation은 noisy컨디션에서 한계가 있긴 있었다.

- Motion Planning : Move it활용, manipulation에 Move it은 매우 유용한 것으로 보인다.

- Robot motion : this way for the picking
