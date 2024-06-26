# Image-Distortion-Correction
딥러닝 모델을 활용한 이미지 왜곡 보정 알고리즘 제안 및 왜곡 측정 평가지표 제안

### Background
오늘날, SNS 발달 및 카메라 기술 발달으로 많은 사람들이 본인의 사진을 공유하는 것이 일상화가 되었다. </br>
이 과정에서 사진 보정 기술 또한 발전했으며, 어플리케이션도 많이 출시되었다. </br>
보정을 진행할 시에 불필요한 왜곡이 발생하는 부분 없이 원하는 객체만 보정할 수 있는 알고리즘을 제안하고자 한다.</br>


### Stacks

[언어] - Python</br>
[프레임워크 및 라이브러리] - PyTorch, OpenCV</br>
[모델] - OneFormer, MatteFormer, Lama, Real-ESRGAN</br>

### FLOW
1. Segmentation - OneFormer 구현 후 segementation 성능 향상을 위해 MatteFormer 추가 구현</br>
2. Image Inpainting - Lama 구현
3. 합성 - OpenCV 사용
4. Image Resolution - Real-ESRGAN 구현
5. COCO 2017 Train 중 'Person'으로 라벨링 된 701장의 이미지 추출
6. 보정 어플리케이션을 사용해 부위 5개, 보정 방향 2개, 보정 수치 2개를 기준으로 4528장의 왜곡 이미지 생성
7. 본 프로젝트에서 제안하는 알고리즘으로 왜곡이 보정된 이미지 4528장 생성
8. 평가지표 제안(DLS, P2P)

  
### Review
처음으로 생각했던 아이디어를 딥러닝 모델을 활용해 구현하는 프로젝트였다는 점에서 의미있었다.</br>
SOTA 모델을 구현하는 과정에서 오류가 많았으나 팀원들과 고민하고 함께 해결해나가는 과정에서 모델 구현 능력을 향상시킬 수 있었던 것 같다.</br>
개인적인 스케줄이나 학업 문제로 중간중간 쉬었던 기간이 있어 이 프로젝트에만 몰두할 수 없었다는 점이 조금 아쉽다.