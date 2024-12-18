# Face Mack Detection
사진을 보고 이 사람이 마스크를 꼈는지 확인하는 프로그램입니다.

우선 마스크를 끼고 있거나 끼고 있지 않은 다양한 사진을 수집하여 Face Mask Detection이라는 폴더를 생성하였습니다. 

Face Mask Detection이라는 폴더 안에는 image와 annotation이라는 폴더가 있는데 images 폴더에는 0부터 852번까지의 이미지 파일이 있으며 annotations 폴더에는 이미지 파일의 정보를 가지고 있는 xml 파일이 0부터 852번까지 있습니다. 

전체 데이터셋 개수가 853개로 조금 적다고 생각해 8대 2의 비율로 시험 데이터를 만듭니다. 853개의 데이터 중에서 170개를 시험 데이터로 사용하기 위해 이들을 별도의 폴더 test_images와 test_annotations 폴더에 랜덤하게 옮겨주었습니다.

이 후 이 데이터와 torchvision.model 모듈을 통해 학습을 진행하였고 마스크를 쓴 얼굴에는 초록색 박스, 애매한 경우 노란색 박스, 쓰지 않은 얼굴에는 빨간색 박스가 그려지도록 하였습니다.

학습을 마친 이후 이미지 중 하나를 불러와 최종 테스트를 진행하였습니다.

추가로 미리 훈련된 모델(OpenCV DNN 기반 Face Detector)을 사용하여 이 모델은 어떻게 작동하는지 확인하기 위해 이에 대한 코드도 작성하였습니다.
