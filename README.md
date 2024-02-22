# [ 대구 개발자 연봉에 대한 현황분석과 원인분석 ]


## 대구 개발자 연봉에 대한 현황분석


**정말 대구 개발자 연봉은 타지역에 비해 낮은 걸까?**


### (1) 데이터 확인 및 생성

- 지역별 전체 평균 월급 및 임금 상승률 데이터(2020-2023) 생성
- 지역별 개발자 평균 월급 데이터 생성
- 지역별 개발자 한달간 평균 근로시간 및 근로일수 데이터 생성
- 데이터 가공 후
    - 2020 ~ 2023년간 개발자 임금 상승률 데이터 생성
    - 전국 평균 임금상승률 데이터 생성 
    - 광역시 별 비교를 위한 광역시 한정 데이터 생성
        - 광역시 별 개발자 평균 월급 데이터 생성
        - 광역시 별 개발자 평균 근로시간 및 근로일수 데이터 생성


### (2) 데이터 가공

- 인덱스명이나 컬럼명을 통일
    - 지역 이름을 같게 통일함 ex) 강원특별자치도 -> 강원도
- 데이터 표준화 및 결측치 제거
    - '-'값을 nan값으로 대체 후 dropna() 실행 
- 지역별 평균 임금 상승률 컬럼과 년도별 평균 임금 상승률 행 추가
    - 전국과 대구광역시 임금 상승률 비교
    - 년도별 대구광역시 임금 상승률 파악
- 지역별 개발자 평균 월급 데이터를 통해 전년도 대비 임금 상승률 DF 생성
    - 2021년 임금 상승률, 2022년 임금 상승률, 2023년 임금 상승률 DF 생성
    - 확실한 현황 분석을 위해 2020년 대비 2023년 임금 상승률 값 추출
    - 광역시 별 2020년 대비 2023년 임금 상승률 DF 생성
- 대구를 포함한 타 광역시 인덱스만 따로 concat을 통해 병합
    - 광역시 별 개발자 평균 임금 DF 생성
    - 광역시 별 개발자 평균 근로시간 및 근로일수 DF 생성


### (3) 그래프 결과


![평균 월급 대비 개발자 월급](https://github.com/ParkHeeJin00/KDT-5_PublicDataProject/assets/155441547/e8960fdd-1e7c-44d6-99b9-1d8adc31c951)



![임금상승률](https://github.com/ParkHeeJin00/KDT-5_PublicDataProject/assets/155441547/4801311b-a391-4362-857b-e2c81de0c5fe)



![지역별 평균 연봉](https://github.com/ParkHeeJin00/KDT-5_PublicDataProject/assets/155441547/f18448a1-875b-46b9-83cd-fbc898d13e66)



![개발자 임금상승률](https://github.com/ParkHeeJin00/KDT-5_PublicDataProject/assets/155441547/467e9d90-7571-4943-8800-a9c61172b835)



![개발자 평균 월급](https://github.com/ParkHeeJin00/KDT-5_PublicDataProject/assets/155441547/c3b763cb-7597-44ee-af24-feaf24aa6157)


![광역시별 개발자 평균 임금](https://github.com/ParkHeeJin00/KDT-5_PublicDataProject/assets/155441547/19b77874-4387-4671-8e6b-0cba11477cae)



![개발자 평균 근로일수](https://github.com/ParkHeeJin00/KDT-5_PublicDataProject/assets/155441547/23c98064-225d-40f5-a3a9-8aa567e150a9)




### (4) 그래프 결과 분석

전국 평균에 비해 대구광역시의 임금 상승률이 높아보이지만, 그것은 대구광역시의 절대적인 평균 임금이 적기 때문이다. 세종특별자치시에 공무원이 많이 거주하기 때문에 공무원의 월급으로 월급의 많고 적음을 기준하고자 수직선을 추가하였다. 대구광역시 평균과 세종특별자치시 평균의 수직선을 봤을 때, 대구광역시의 평균이 매우 적음을 알 수 있다. 앞선 그래프는 전 직종의 임금 상승률이기 때문에 개발자의 임금 상승률을 보고자 데이터를 가공했다. 광역시끼리 비교했을 때, 울산광역시 다음으로 개발자 임금상승률이 매우 낮음을 확인할 수 있다. 지역별 개발자 평균 월급은 중위 수준에 머무는 것 같지만 광역시 별로 비교하면 상대적으로 낮은 수치임을 파악할 수 있다. 워라밸은 임금과 반비례한다. 따라서 절대적인 근로시간이나 근로일수가 적다면 임금이 적은 것은 당연하다. 따라서 지역별 개발자의 한달 간 평균 근로시간과 근로일수를 비교해보았다. 대구는 타 지역에 비해 평균 근로일수도 많은 편이다.


### (5) 인사이트 도출

대구 개발자의 임금은 타 지역보다 낮은 편에 속하며 한달 간 평균 근로일수도 타 지역보다 긴 편에 속한다. 대구 개발자의 근무조건이 타 지역에 비해 열악함을 알 수 있다. 따라서 타지역으로의 청년 인구 유출률이 높음을 예상할 수 있다.


### (6) 피드백

x축, y축에 대한 라벨이 있었으면 좋았겠다.(다른 팀원에게)


### (7) 내 생각

찾은 데이터 내에서 뽑을 수 있는 인사이트는 최대로 뽑은 것 같다. 다만 아쉬운 점은 개발자 임금에 시니어 임금도 모두 포함되어 평균치가 높게 나와 주니어의 임금을 알기 어렵다는 점이다. 지역별 개발자의 초봉 데이터가 있었다면 대구의 낮은 개발자 임금이 더욱 직관적으로 보여질 수 있을 것 같다.


### (8) 결론

<aside>
💡 실제로 대구의 개발자 임금이 타 지역에 비해 절대적으로 낮은 것이 맞다.

</aside>
