# DACON_JobCare
![20220524_111648](https://user-images.githubusercontent.com/84311270/169935211-c1ce462c-ba79-4ee4-9c34-f265e1b26d4d.png)  
잡케어 서비스에 적용 가능한 추천 알고리즘 개발하는 것이 목적이였다.

## Dataset

train.csv  
 	d_l_match_yn :  속성 D 대분류 매칭 여부  
 	d_m_match_yn :  속성 D  세분류 매칭 여부  
 	d_s_match_yn :  속성 D  코드 매칭 여부  
 	h_l_match_yn :  속성 H 대분류 매칭 여부  
 	h_m_match_yn :  속성 H 중분류 매칭 여부  
 	h_s_match_yn :  속성 H 코드 매칭 여부   
 	person_attribute_a :  회원 속성 A  
 	person_attribute_a_1 :  회원 속성 A 하위 속성 1  
 	person_attribute_b :  회원 속성 B  
 	person_prefer_c :  회원 선호 속성 C  
 	person_prefer_d_1 :  회원 선호 속성 D 1번  
 	person_prefer_d_2 :  회원 선호 속성 D 2번  
 	person_prefer_d_3 :  회원 선호 속성 D 3번  
 	person_prefer_e :  회원 선호 속성 E  
 	person_prefer_f :  회원 선호 속성 F  
 	person_prefer_g :  회원 선호 속성 G  
 	person_prefer_h_1 :  회원 선호 속성 H 1번  
 	person_prefer_h_2 :  회원 선호 속성 H 2번  
 	person_prefer_h_3 :  회원 선호 속성 H 3번  
 	contents_attribute_i :  컨텐츠 속성 I  
 	contents_attribute_a :  컨텐츠 속성 A  
 	contents_attribute_j_1 :  컨텐츠 속성 J 하위 속성 1  
 	contents_attribute_j :  컨텐츠 속성 J   
 	contents_attribute_c :  컨텐츠 속성 C   
 	contents_attribute_k :  컨텐츠 속성 K  
 	contents_attribute_l :  컨텐츠 속성 L  
 	contents_attribute_d :  컨텐츠 속성 D  
 	contents_attribute_m :  컨텐츠 속성 M  
 	contents_attribute_e :  컨텐츠 속성 E  
 	contents_attribute_h :  컨텐츠 속성 H  
	person_rn :  사용자번호  
 	contents_rn :  컨텐츠번호  
	contents_open_dt :  컨텐츠 열람 일시  
 	target :  컨텐츠 사용 여부 (라벨)  
  
test.csv  
참가자 제공 레이아웃.pdf : 데이터 컬럼에 대한 세부 설명  
속성_D_코드.csv   
속성_L_코드.csv  
속성_H_코드.csv  

## Model
data와 속성 코드를 매칭시키고 이상치에 대해 전처리르 진행하였으며 TabNet 모델과 다양한 Machine Learning 모델을 사용하였으며 최종적으로 Catboost 모델을 사용하였다. 그리고 Kfold를 사용하여 교차검증을 진행하였고 threshold를 변경하며 최적의 threshold를 찾는 방향으로 진행하였다.

## Results
Public Score : 0.70178, Private Score : 0.70319로 최종 73등으로 상위 10% 안에 들며 대회를 마무리하였습니다.
![20220524_111800](https://user-images.githubusercontent.com/84311270/169936597-512c76cd-fe92-44d7-8126-10459dd2a287.png)

