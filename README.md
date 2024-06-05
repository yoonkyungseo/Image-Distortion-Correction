# Image-Distortion-Correction


### Background
오늘날, 남녀노소 가리지 않고 연락을 주고 받을 때, 이모티콘을 사용한다. </br>
하지만 상황에 맞는 이모티콘과 원하는 이모티콘을 사용하기 위해선 여러 이모티콘을 구매해야 한다. </br>
자신의 감정을 담은 얼굴 사진으로 원하는 애니메이션 캐릭터 그림체로 다양한 감정을 전달해보자.

![image](https://user-images.githubusercontent.com/103553532/209472015-b0b7c5a3-f436-4819-9479-fde0bcb28d7e.png)

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