# 2022-Sunrin-Ai-Project
2022 선린 인공지능 교과 1학기 프로젝트

# 개요
- 프로젝트 주제 : 인스타그램의 스팸/가짜 계정과 진짜 사람 계정을 구분하는 인공지능 구현하기
### 기술 스텍
- Python
- Pandas
- Numpy
- Matplotlib
- Sklearn
- Decision Tree Classifier
- K Neighbors Classifier

# 팀원
- 박희찬 ([ckstmznf](github.com/ckstmznf))
- 여준혁 ([secon0101](github.com/secon0101))


# 계획
### 데이터 수집
- 플랜 A : Selenium을 사용한 인스타그램 크롤링
- 플랜 B : Kaggle 오픈 소스 사용 [(바로가기)](https://www.kaggle.com/datasets/free4ever1/instagram-fake-spammer-genuine-accounts)
> 결과 : 크롤링에 성공했지만 데이터가 깔끔하지 않고, 모델 학습이 잘 되지 않아서 플랜 B 사용
- [데이터 바로가기](https://github.com/ckstmznf/2022-Sunrin-Ai-Project/blob/main/user_info.csv)

### 모델 학습
- 결정트리 알고리즘과 K최근접 이웃 알고리즘 두 알고리즘 모두 다 사용해서 각각의 모델 제작
- 학습에 사용 하는 독립 변수로 다음 데이터 재공
    - profile pic : 계정의 프로필 사진 여부
    - nums/length username : 계정 이름의 숫자, 문자의 비율
    - fullname words : 계정 이름의 단어 수
    - nums/length fullname : 계정 이름에서 숫자가 차지하는 비율
    - name==username : 사용자 이름과 계정 이름이 같은지
    - description length : 계정 설명의 길이
    - external URL : 계정의 외부 링크가 있는지
    - private : 계정이 비공개인지
    - #posts : 게시물 수
    - #followers : 팔로워 수
    - #follows : 팔로우 수
