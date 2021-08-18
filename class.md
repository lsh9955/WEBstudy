!참고문헌
https://ko.javascript.info/class

## 1. 클래스 기본 문법
```javascript
class MyClass {
  constructor() {...}
  method1() {...}
}
```

* constructor?  
객체의 기본 상태를 설정해주는 생성자 메서드임.  
new에 의해 자동으로 호출됨. 특별한 절차 없이 객체 초기화가 가능  


## 2. class란?
 자바스크립트에서는, 함수의 한 종류임.
 * class Name {...} 가 하는 일  
 1. Name 이라는 이름을 가진 **함수**를 만듬
 2. 함수 본문은 constructor ? constructor 에서 가져옴 : 본문이 비워진 채로 함수가 만들어짐
 3. 클래스 내에서 정의한 매서드를 Name.prototype에 저장함.
 4. 그래서 Name === Name.prototype.constructor true임

! class 함수 내부엔 [[FunctionKind]]:"classConstructor" 가 붙음    
자바스크립트가 이 프로퍼티가 있는지 확인하기 때문에    
new와 함께 호출하지 않으면 에러가 발생함.  
 
 
## 3. class의 특징  
1. 클래스 매서드는 열거할 수 없음.  
2. 클래스는 항상 엄격 모드로 실행함.  
3. 클래스 표헌식에 이름을 붙이면, 이 이름은 클래스 내부에서만 사용가능  
4. 동적으로도 클래스 생성이 가능함.=>무슨 말인지 모르겠음  

## 4. getter & setter  
* 이게 뭐임?    
  객체 데이터에 직접 접근하는 것을 막기 위해, 메소드를 통해 데이터를 변경하도록 함.  
  setter - 외부에서 메소드를 통해 데이터에 접근하도록 유도  
  getter - 메소드로 필드값을 가공 후 외부로 전달  
  계산된 프로퍼티 - []를 이용해서 객체의 변수명에 미리 계산된 변수를 넣는게 가능함.  
  ```javascript
  let a = 'age';
  const user = {
  name : 'Mike',
  [a] : 30 // age : 30 과 같은 의미
  }
  ```
* 클래스는 getter나 setter, 계산된 프로퍼티를 포함할 수 있음  
