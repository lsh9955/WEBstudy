! 내용 참조 
  1. https://developer.mozilla.org/ko/docs/Web/JavaScript/Guide/Working_with_Objects
  2. https://poiemaweb.com/js-object


## 0. 메소드 정의
객체의 프로퍼티 중 함수인 것  

## 1. this?
해당 메소드가 속한 개체를 가리킴  
따라서 메소드 내부에서 this를 사용하면 객체에 접근 가능  
* this를 쓰는 이유?  
  외부 변수를 사용하면, 값이 변했을 때 참조값이 달라짐.  
* this의 값?  
  런타임에 결정됨. 매서드를 호출 할 때 사용된 객체를 나타냄  
* 화살표 함수?  
  고유한 this를 가지지 않음. 일반 외부 함수에서 this값을 가져옴
!매서드 내부에서 써야함. 그렇지 않고 함수로 호출이 되면 undefined가 됨.  

  
