# 💪 칼로리 소모량 예측 프로젝트

사용자의 신체 정보 및 운동 데이터를 기반으로 소모된 칼로리를 예측하는 머신러닝 모델을 실습합니다.

## 📂 데이터셋

  - `exercise.csv`: 사용자별 운동 데이터 및 칼로리 소모량 기록
  - **GitHub Repository**: `https://github.com/thiskorea81/exercise.git`

## 📊 속성 정보 (Attribute Information)

| 속성명 (영문) | 속성명 (한글) | 설명 |
| :--- | :--- | :--- |
| `User_ID` | **사용자\_ID** | 사용자를 식별하는 고유 번호 |
| `Gender` | **성별** | `male`(남성), `female`(여성) |
| `Age` | **나이** | 사용자의 나이 (세) |
| `Height` | **키** | 사용자의 키 (cm) |
| `Weight` | **몸무게** | 사용자의 몸무게 (kg) |
| `Duration` | **운동\_지속\_시간** | 운동을 지속한 시간 (분) |
| `Heart_Rate` | **심박수** | 운동 중 평균 심박수 (분당) |
| `Body_Temp` | **체온** | 운동 중 체온 (°C) |
| `Calories` | **소모\_칼로리** | 운동으로 소모된 칼로리 (kcal). **(예측 대상)** |

## 🚀 구글 코랩(Google Colab)에서 실행하기

구글 코랩 환경에서 아래 코드를 순서대로 실행하여 데이터를 간편하게 불러올 수 있습니다.

### 1\. GitHub 저장소 복제

`!git clone` 명령어를 사용하여 GitHub에 있는 데이터 파일을 코랩 환경으로 가져옵니다.

```python
!git clone https://github.com/thiskorea81/exercise.git
```

### 2\. Pandas로 데이터 불러오기

저장소 복제가 완료되면, `pandas` 라이브러리를 사용하여 `exercise.csv` 파일을 DataFrame으로 불러옵니다.

```python
import pandas as pd

# 복제된 폴더 안의 파일 경로를 지정합니다.
file_path = '/content/exercise/exercise.csv'

# CSV 파일을 DataFrame으로 읽어옵니다.
# 한글 파일명이 있거나 깨짐 방지를 위해 encoding='cp949' 옵션을 추가할 수 있습니다.
df = pd.read_csv(file_path, encoding='cp949')

# 데이터의 첫 5행을 출력하여 잘 불러왔는지 확인합니다.
df.head()
```
