# traveling_recommendation
사용자 성격 기반, 사용자 현재 기분 기반, 여행지 테마(성향) 기반 여행지 추천 시스템

- 기술 스택: tensorflow, pandas, numpy,
1. 개인 성향 데이터: MBTI, 개인 성격에 따른 여행지 만족도 관련 연구 논문 바탕으로 설문지 문항 구성
2. 개인 감정: 사용자 업로드 사진 3장을 통한 감정 분석(행복, 슬픔, 화남, 중립)
   - 사용 모델: open_cv 얼굴 인식 모델, CNN
4. 여행지 리뷰 텍스트 테마 분류: 레저/체험, 자연, 교육(by softmax)
   - 사용 모델: BERT
5. 여행지 추천 모델
    - INPUT: 개인 성향 설문, 여행지 분류 SOFTMAX DB, 감정 라벨링 데이터
    - 사용 모델: DNN
    - OUTPUT: 여행지 추천 여부
# 모델 구성
<img width="956" alt="모델구성1" src="https://user-images.githubusercontent.com/58072776/132265635-fc92168e-eb56-4a40-a987-367ae6cf130d.PNG">
<img width="955" alt="모델구성2" src="https://user-images.githubusercontent.com/58072776/132265665-e7621608-e28c-4ea3-815e-9bdc94379f5e.PNG">
<img width="955" alt="모델 구성3" src="https://user-images.githubusercontent.com/58072776/132265669-40297e23-fc62-4d38-825e-ac614fab9408.PNG">
