# EveryRegEx
![EveryRegEx](https://github.com/maga32/EveryRegEx/assets/98816249/062689ad-1f07-4714-8a94-bf9dfc03c999)


###
## 0. EveryRegEx? 
- 개발을 하면서 정규표현식(Regular Expression)이 필요한 일이 종종 발생합니다.
- 그때마다 수식을 다시 찾아보면서 표현식을 만들고 테스트 하는 일에 지쳐서 개발하게 되었습니다.
- EveryRegEx는 정규표현식을 보다 쉽게 만들어 낼 수 있는 도구입니다.


###  
## 1. 링크
> [EveryRegEx](https://everyRegEx.sung-a.duckdns.org/)


###
## 2. 사용법
- 조건 란에 필요한 조건들을 적고, 테스트 란에 테스트 할 내용을 적으면 결과가 도출됩니다.

### 2.1. 조건
- 조건 란은 직접 적으시거나 위의 단축버튼을 눌러서 적을 수 있습니다.
- 조건 란에는 엔터나 탭 등을 이용하여 보기 편하신대로 띄어 적으셔도 하나의 표현식으로 계산됩니다.
- 각 조건의 설명과 예제는 조건설명을 클릭하여 확인하실 수 있습니다.
- 조건 작성시 해당 조건의 표현식이 보여집니다. 표현식 클릭시 클립보드에 복사됩니다.

### 2.2. 테스트
- 테스트 란에는 조건 란에 적은 조건을 바탕으로 테스트 해보실 문구를 적어주세요.
- 테스트 란은 엔터를 기준으로 각각의 문장을 테스트를 해보실 수 있습니다.

### 2.3. 결과
- 결과 란에서는 조건과 테스트를 기반으로 작성한 정규표현식에 각각의 문장이 해당되는지 확인하실 수 있습니다.
- 조건에 일치하는 부분은 초록색, 일치하지 않는 부분은 빨간색으로 나타나게 됩니다.


###
## 3. 예제
### 3.1. 전화번호 찾기
- 조건
```javascript
.숫자().횟수반복(2,4)
.일치("-")
.숫자().횟수반복(3,4)
.일치("-")
.숫자().횟수반복(4)
```
- 테스트
```
010-1234-5678
안녕하세요 010-000-2345 테스트입니다
서울 전화번호 02-123-4567
020-3333
```
### 3.2. 네이버메일 찾기
- 조건
```javascript
.존재().일치("@naver.com").끝()
```
- 테스트
```
test123@hanmail.net
test123@naver.com
test123@naver1.com
@naver.com
test123@naver.coms
```

###
## 4. 기타정보
- 위 페이지는 Bootstrap의 css를 사용하고 있습니다. https://getbootstrap.com
- 위 페이지는 VerbalExpressions에 의존합니다. https://github.com/VerbalExpressions