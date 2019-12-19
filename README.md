2015108199 이민재

별똥별 데이터를 활용하여 별똥별 위치와 속도 예측

- kaggle 에서 제공하는 Fireballs 데이터를 이용하여 별똥별의 위치와 속도를 예측한다.
- PredictionUtil 라이브러리를 활용한다.
- 데이터 : https://www.kaggle.com/nasa/fireballs/data

1. 데이터 불러오기
 ```
from prediction_util import PredictionUtil

gildong = PredictionUtil()
gildong.read('cneos_fireball_data.csv')
gildong.show_unique_column()
```

![11](https://user-images.githubusercontent.com/54211648/71184985-e8e97a00-22bd-11ea-9464-ef92da3ebcfe.JPG)

데이터가 각각 별동별의 위도, 경도, 고도, xyz 위치 등을 나타내므로 데이터를 삭제하지 않는다.

2. 데이터 분석하기
PredictionUtil 라이브러리 에 있는 기능들을 사용해 데이터를 그래프로 표현.

```
gildong.heatmap(['Latitude (deg.)','Longitude (deg.)','Altitude (km)','Velocity (km/s)','vx','vy','vz'])
```

![22](https://user-images.githubusercontent.com/54211648/71185764-69f54100-22bf-11ea-892b-a0d249a89bac.JPG)
