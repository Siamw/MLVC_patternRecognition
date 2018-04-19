# 1. Intro

## 1.1 왜 패턴인식인가?
- 뇌 과학 분야 : 사람의 뇌가 어떻게 인식을 수행하는지를 알아내는 연구
    - 간단한 연산을 담당하는 엄청난 수의 뉴런이 상호 연결되어 신호를 주고받는다.
    - 컴퓨터 : 정보 처리가 순차적이며, 뇌의 정보 처리방식과는 근본적으로 차이가 존재한다. 
- 지능 기계의 예 (기존 제품 + 인식기능)
    1. 우편물 분류기 : 바고드, 우편번호, 주소 높은 정확률로 인식
    2. PDA 필기 입력기 : 터치스크린에 전자펜으로 필기 - 2차원 이상의 궤적 인식 필요
    3. 동작 인식 핸드폰 : 핸드폰을 쥐고 동작함으로서 특정 명령 내림 - 3차원 궤적 인식
    4. 지문 인식 마우스, 과속 단속기, 청소로봇 등
- 응용 분야 
    1. 공장 자동화, 문자 인식, 음성인식 (기계에 명령을 내리기에 미래 인터페이스로 중요) , 자연어 처리
    2. Data mining : 대용량 불완전 자료에서 유용한 지식을 찾는 것.
        - 고객 관리, 웹 관리, DB관리 등에 필수적인 기술. 
        - 효율적인 특징 추출, 분류, 군집화 알고리즘 절실
    3. 정보 검색, 사람 컴퓨터 인터페이스(사람의 움직임, 음성 이용하여 작동), 생체인식 (보안), 지능 교통 시스템
    4. 생물 정보학 : 생물학 분야의 대용량 자료에서 생명 현상의 규명에 필요한 지식을 추출하는 것을 목표로 함.
        - 손실 정보나 비수치( nonnumeric ) 자료 등을 적절히 다룰 수 있어야 함.
    5. 지능 로봇 : "상황 인식"이 핵심
    
    ## 1.2 어떻게 인식하나?
    - 패턴 인식의 처리 과정 :    패턴 -> 특징*( feature ) -> 분류*( classification ) -> 부류
    <pre><code>
    숫자를 적는 칸 : 0~9, 10 종류의 pattern 발생
    이 때, 10 종류의 숫자 각각 : 부류( class )
    부류의 개수 M =10, 부류 = w1,w2, ... , wm
    </code></pre>
    - 패턴 원천 ( pattern source ) : 패턴을 발생시키는 도메인.
        ex) 은행의 전표를 인식하는 시스템 : 매일 수많은 고객에 의해 전표 작성, 필기 숫자 패턴 수시로 발행.
    - 