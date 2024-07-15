# B.S_AI_Project
시각 장애인을 위한 화장품 패키징 OCR 모델

### About the project

- **시각 장애인을 위한 화장품 패키징 OCR 학습모델 AI**
- 시각 장애인들이 화장품 식별을 할 수 있도록 제품의 패키징 속 정보(글자)를 읽고, 유해성분 혹은 원하는 성분을 검출하는 AI기술을 통해 사회적 가치를 실현하고자 함
- Tensorflow나 keras, Pytorch에서 제공하는 전이 학습 신경망 클래스를 사용하지 않았으며, 주어진 학습 데이터를 가지고 직접 모델을 구현하며 Task를 진행

### Summary

1. 데이터 정의 및 수집 : AI hub에서 화장품, 의약품 패키징 OCR 학습 데이터(image:json) 활용
2. EDA를 통한 학습 데이터에 대한 분포 및 특성 확인 ≫ 프로젝트 목적에 맞는 전처리 방향 설정
3. 데이터 전처리 
    - json 원천 파일에서 label, Bbox 정보만을 추출 및 저장
    - Bbox의 Text 좌표 값을 할당하여 좌표 지정 Image crop 진행
    - Cropped Image의 path list와 각 Image에 대한 text label list → 모델의 입력 데이터 완성
4. 모델 정의 및 학습 :  RCNN 모델 채택 → CNN을 통한 이미지 추출, RNN을 통한 텍스트 전처리 + Fully connected layer가 OCR 수행에 탁월할 것이라 판단.
5. RCNN 모델 구현 및 최적 파라미터 설정을 통해 Accuracy 제시, 성능 최적화

### Role

- 팀장으로서 원활한 프로젝트 수행을 위해 task 분담 및 전체적인 workflow 관리
- 데이터 전처리 및 모델링 전 과정 전담
- CNN 적층 모델 구현 및 최적 파라미터 실험

### Results

- 클래스 프로젝트 점수 1위
- Accuracy 70.06

[BMA_Project_3조_결과보고서.pdf](https://github.com/user-attachments/files/16239784/BMA_Project_3._.pdf)
[BME 인공지능 프로젝트_OCR.pdf](https://github.com/user-attachments/files/16239783/BME._OCR.pdf)
