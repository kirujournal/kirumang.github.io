Reading Group (15.11.2016)
### Incremental Scene Understanding on Dense SLAM
- Single View Approach의 한계를 조목조목 깐다
   1. Occlusion
   2. Differ from every side by side
   3. Same appearance in the scene but different object
      (but can be distinguished by other side)
- Fig2 가 전체 내용을 한방에 정리해준다.

- the idea : global map -> current frame mapping
    - is one of my idea of research
      (CCTV global map -> robot view mapping)
      -> I can think about this and want to realize this as my own code
- New RGB Frame is coming
- Tree 구조를 이용하여 Incremental Semantic Segmentation을 수행
  -> Temporal Hypothesis Tree라고 해서 Segmentation조각을 object로 merge해 나감
- Pose Estimation은 ObjRecRanSanc을 사용함.
   - ref : "An efficient RANSAC for 3d object recognition in noisy and occluded scenes", 2011
-
