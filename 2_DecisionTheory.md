# 1. Decision Theory

## 2.1 확률과 통계
- X = 랜덤변수.     주사위를 던졌을때 3이 나올 확률  P(X=3) = 1/6 
- 연속적인 값을 가질 때 : 확률 밀도 함수 ( probability density function )로 표현
- 조건부 확률 ( conditional probability ) : A에서 white가 뽑힐 확률 P(Y=white | X=A) = P(white | A)
- 결합 확률 ( product rule ) : 상자는 A, 공은 white가 뽑힐 확률 P(A, white) = P(white|A)P(A) - 곱 규칙 ( product rule )
- 주변 확률 ( marginal probability ) : 합 규칙에 의한 확률
- 독립 ( independent ) : 두 랜덤 변수가 서로 영향을 미치지 않는 경우
- 사후 확률 ( posterior probability ) : Y가 고정되고, X에 따라 확률을 계산. 즉 사건 Y가 일어난 후에 따지는 확률
- 베이스 정리 (Bayes rule) : P(A|white) = P(white|A)*P(A)/P(white)
- 평균 mean, 분산 variance, 표준편차 standard deviation 

## 2.2 베이시언 분류기
- 베이스 정리를 이용하여 사후 확률(특징 공간이 무수히 많은 점을 가지므로 이들 모든 점에 대해 확률을 표현할 수 없다.)을 다른 것으로 대치하여 계산
- p(wi|x)=p(x|wi)p(wi)/p(x) = 우도 * 사전확률 / p(x)
- 최소 오류 베이시언 분류기 (minimum error Bayesian classifier)  
        P(x|w1)P(w1) > P(x|w2)P(w2)이면 X : w1 로 분류, 반대면 w2로 !
- 최소 위험 베이시언 분류기 (minumum risk Bayesian classifier)  
        x를 q2>q1이면 w1로 분류, 반대면 w2로 분류  
        이 때,    q1 = c11 p(x|w1)P(w1) + c21 p(x|w2)P(w2)  
                    q2 = c12 p(x|w1)P(w1) + c22 p(x|w2)P(w2)  
        우도비 결정 규칙 ( likelihood ratio decision rule )을 사용하여 나타내면,  
        p(x|w1) / p(x|w2) >T 이면 x를 w1로 분류,  반대면 w2로 분류.  
        이 때 , T = (c21-c22)P(w2) / (c12-c11)P(w1)
- 우도비 ( likelihood ) : 두 우도의 비율 p(x|w1)/p(x|w2)
- M 부류 최소 위험 베이시언 분류기 ...

## 2.3  분별 함수
- 분별함수 ( discriminant function ) : x를 서로 다른 부류로 분별하는데 필요한 정보를 제공해주는 것
    - 서로 다른 여러 분류기를 일반적인 틀에 넣어 해석할 수 있다.
    - 확률 값이나 손실 값 그 자체가 아니라 그들 사이의 상대적인 크기를 비교하여 의사 결정을 한다.
    
## 2.4 정규 분포에서 베이시언 분류기
- 훈련 집합이 정규분포와 비슷하게 나왔다고 가정하고, 이를 정규분포 ( 가우시언 분포 Gaussian distribution )로 모델링하여 베이시언 분류기를 만들어보자.
- 선형 분별 분석 ( linear discriminant analysis ) : 모든 부류가 같은 공분산을 갖는다는 가정하에 결정 경계를 위한 수식을 유도하여 선형 분류기를 얻음
- 2차 분별 분석 ( quadratic discriminant analysis ) : 공분산 행렬에 아무런 재약이 없고, 선형 분별 분석과 비슷한 과정을 거쳐 분류기를 얻음.
- 두 부류의 사전확률 = 공분산 행렬 가정
                    
