### 관리자
1. 레이아웃
    - 프레임
    - 페이지
    - 컨텐츠
2. 배너
3. 통계
4. 컨디션
5. VIEW

---

### 페이지 구성
- 전역변수
    - 전역으로 참조가 필요한 데이터 저장
    - 각 라이브러리 간 공유 데이터 저장
- FRAME
    - `FRAME` 은 페이지당 1개만 사용가능
- LIBRARY
    - 각 페이지는 라이브러리의 집합으로 구성
- VIEW

---

### AJAX 관리
- SERVER MIDDLEWARE
- `FRONT`에서 호출할 때 `/ajax`로 호출
- 호출 시 `ajaxId` 값을 전송
- `ajaxId` 값에 따라 특정 라이브러리와 연결
- 진입 포인트를 하나로 관리
- 데이터 반환 포인트도 하나로 관리

---


### BACK => FRONT 데이터 구조
- JSON

```FRAME
FRAME
    LayoutKey: { // 사용할 레이아웃 ID
        data: {
            // 레이아웃 고정 데이터
        },
        contents: {
            // 레이아웃 내 동적 레이아웃
            LayoutKey: { // 사용할 레이아웃 ID
                data: {
                    // 해당 레이아웃에서 사용할 데이터
                }
            }
        }
    }
```
---
### LIBRARY
- 각 기능을 정의

---

### LAYOUT 관리자
- 