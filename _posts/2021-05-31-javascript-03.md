---
layout: post
title: "javascript(2) - 창 띄우기와 형 변환"
tags: [자바스크립트, 메서드, 형변환]
comments: true
---

브라우저의 경고/확인 창을 띄우는 메서드와 데이터 형 변환시키기

--- 

## **Prompt Method**
창을 띄우다 라는 뜻으로, 간단한 메세지가 담긴 창을 띄우거나 질문에 대한 답을 받을 수도 있다<br />
```javascript
prompt('내용') // 기본형식
```
```javascript
/*응용*/
let age = prompt("나이를 입력하세요","20"); // 나이 질문 응답창
let gender = prompt("성별을 입력하세요","여"); // 성별 질문 응답창
let result = age>=20 && gender == "여"; // 필터링 조건 (true or false값)
document.write(result); // 결과 화면출력
```
위의 스크립트를 작성하면 질문과 질문에 응답할 수 있는 팝업 창이 뜨고, 조건에 맞는 답을 입력한다면 true, 아니라면 false가 화면에 나타난다 

<br />

## **Confirm Method**
확인과 취소 중 선택할 수 있는 창을 띄울 수 있으며, '확인'을 선택할 시 true값을 반환하고 '취소'를 선택할 시 false값을 반환한다
```javascript
confirm('내용')
```
```javascript
const question = confirm('Are you okay?');
const answer = question ? 'Good!' : 'Cheer up!';
document.write(answer);
```

***
## **Number Method** 
문자형식로 입력된 숫자 데이터를 숫자형식으로 바꿔준다<br />
**문자로 입력된 데이터에 숫자만 들어있어야 함*
```javascript
Number()
``` 
```javascript
const popul(Number('100'));
console.log(popul); // 100 출력
```
위의 스크립트를 작성하면 입력된 '100'이라는 문자 데이터를 숫자로 변환시켜준다

<br />

## **parseInt** 
문자형식로 입력된 숫자 데이터를 숫자형식으로 바꿔준다<br />
**문자로 입력된 데이터의 숫자와 문자들 가운데 숫자만 골라서 변환해줌. <br />
단, 숫자가 문장의 가장 앞에 와야 하고 숫자가 띄어쓰기로 여러개 구분되었다면 가장 앞의 숫자만 변환해옴*
```javascript
parseInt()
``` 
```javascript
const popul(parseInt('10 to 30'));
console.log(popul); // 10 출력
```
위의 스크립트를 작성하면 입력된 '100'이라는 문자 데이터를 숫자로 변환시켜준다

<br />

## **parseFloat**
문자형식으로 입력된 숫자 데이터를 숫자형식으로 바꿔준다<br />
**Number나 parseInt와는 다르게 소수점까지 변환해올 수 있으며, 변환할 수 있는 기준은 parseInt와 같다*
```javascript
parseFloat()
```
```javascript
const popul(parseFloat('3.38 percent growth'));
console.log(popul); // 3.38 출력
```