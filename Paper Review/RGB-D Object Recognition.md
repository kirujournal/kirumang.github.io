#  RGB-D Frameworks and Approaches


### From V4R
##### (1) A Global Hypothesis Verification Framework for 3D Object Recognition in Clutter (Aitor Aldoma, 2015)

    이 논문은 Fig.1로 한방에 설명이 되는 논문이다.
    The RGB/RGB-D Local descriptors are extracted from RGB-D Scene
       - RGB : SIFT
       - RGB-D : SHOT
    And Global Descriptors are extracted after segmentation of the scene and analyzed by OUR-CVFH Description as a Feature
    각각의 Local, Global Pipeline을 통해 만들어진 Hypothesis를 하나의 Cost Function으로 가지고 오고, 이 Cost function을 가지고 Object Recognition을 수행하여 3중으로 Scene에 있는 Object에 대한 Recognition Rate를 증가 시키다.

    이것은 어찌보면 Ensemble이라고 불리는 Approach라고 볼 수 있을 것 같다. 다시 말해 여러가지 장/단점이 있는 Classifier에 해당 장/단점에 Weight를 붙여 합치는 것. 이는 각각의 Classifier 단독의 Accuracy를 늘 뛰어 넘을 수 있다는 점

    각각의 Pipeline은 새로울 것은 없어 reference를 많이 파봐야 할 내용이고, 이렇게 다양한 Classifier를 어떻게 Ensemble했는냐가 논문의 주요 내용이 되겠다.
    Global한 Pipeline의 경우 논문에서 한 문장으로 요약된다 ref.4를 보라는 거다


    이 논문이 가정하고 있는 부분과 한계를 따져보면

      1. Model의 full 3D data 를 가지고 있어야 한다.
      그래서 논문에서 사용한 Dataset도 Object에 대한 Modeling 데이터가 있는 것을 사용했는데, 실제 로봇이 Working 하는 Field 는 unknown object가 훨씬 많다.

      2. Only Using Single view - Not Multi view, Registered Point
      Global Pipeline에서 조차도 Global한 3D Map이 아닌 한번의 RGB-D Scene을 가지고 수행을 하기 때문에, Highly Occluded Scene을 극복하기 위해 Multi-view로 로봇탐색을 수행하는 부분이 고려 되어있지는 않다. 로봇이 멀리서 물건을 보고 "아 저기 가야 겠다" 를 생각하는 수준에서 사용 할 수 있을 것으로 보이고, Grasp을 위한 최초의 Planning시에 유용할 것으로 보인다. 아는 물건의 위치와 pose를 아니까 초기에 접근을 쉽게 할 수 있겠지.

      3. 의문점 : Processing 속도, Local/Global을 모두 돌리는데 소요되는 시간은 궁금함. Realtime은 안될 것 같은데 높은 Accuracy와 맞바꾼 것인지.

  * 이 논문을 더 이해 할지, 나만의 길을 개척할지 고민이 필요한 부분. Handwriting feature는 대세는 아니지만, 여전히 자기의 영역에서 최고의 Performance를 보여주고 있음

        Selected Citation in this paper
            [4] Global pipeline : "Multimodal Cue integration through hypothesis verification for RGB-D object recognition and 6DOF pose estimation"

            [15] Local pipeline : "3D Object recognition in cluttered scenes with local surface features"

            [21] 3D Segmentation : "Segmentation of unknown objects in indoor environments"


### From Others
##### Rome

#####
