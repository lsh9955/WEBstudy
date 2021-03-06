! 내용 참조 
  1. https://developer.mozilla.org/ko/docs/Web/JavaScript/Guide/Working_with_Objects
  2. https://poiemaweb.com/js-object

## 1. 객체가 뭐임?
객체-프로퍼티의 모음, 단독으로 존재 가능한 개체(entity)  
프로퍼티와 타입을 가짐  
자바스크립트에서는 null, undefined를 제외한 모든 원시 타입도 객체임    
## 2. 프로퍼티?  
* 프로퍼티-이름(name 또는 key) 과 값(value)의 연결로 이루어짐    
  =객체에 붙은 변수라고 할 수 있음    
* 메소드-프로퍼티 중 값이 함수인 것    
프로퍼티에 접근할 때-도트 표기법을 이용    
```javascript  
objName.propertyName  
myCar.make = "Ford";  
```  
대괄호 표기법도 가능    
객체는 연관배열이라고도 불리는데  
각 프로퍼티는 하나의 문자열 이름과 연관되어 있어서, 그 문자열 이름을 통해 접근이 가능하기 때문. 배열접근과 같은 방식임  
myCar["model"] = "Mustang";  
  
  
 자바스크립트 식별자(identifier)로 적합하지 않으면 (예 : 하이픈, 빈칸을 포함하거나 숫자로 시작하는 이름), 대괄호를 이용한 표기법으로만 접근이 가능  
  
자바스크립트에서는 미리 정의된 객체가 존재함.    
근데 사용자가 추가적으로 객체를 생성할 수 있음.    
객체 이니셜라이저를 이용하거나,     
먼저 생성자 함수를 정의한 후 이 함수와 new연산자를 이용해 인스턴스를 만들수 있음.    
또 이게 뭔소리냐?    
  
객체 이니셜라이저(이니셜라이저라는 것은 초기화라는 뜻임)  
```javascript  
var obj = { property_1:   value_1,   // property_# may be an identifier...  
            2:            value_2,   // or a number...  
            // ...,  
            "property n": value_n }; // or a string   
```  
이러한 방식임.(수식임)  
근데 이 이니셜라이저로 생성된 객체는 서로 별개임.  
즉 객체 이니셜라이저로 만들어진 객체들은 Object의 인스턴스들이 됨.  
이게 뭔소릴까?  
객체는 소프트웨어 세계에 구현할 대상.  
구현하기 위한 설계도-class  
구현된 실체-인스턴스인 것임.  

  
그 다음으론, 생성자 함수를 사용하는 방법이 있다.  
생성자 함수를 작성하여 객체 타입을 정의한다. 이때 이름 첫글자는 반드시 대문자여야한다.  
그 이후 new를 이용하여 객체의 인스턴스를 생성한다.  
객체 타입?    
object type을 객체 타입 또는 참조 타입이라 하는데, 이것은 객체의 모든 연산이 참조값으로 처리된다는 것을 의미함(https://poiemaweb.com/js-object)     
객체는 프로퍼티를 변경할 수 있으니까, 변경 가능한 값임.    
따라서 객체 타입은 동적으로 변화할 수 있는 것임. 어느 정도의 메모리를 차지할 지 알 수 없으므로 런타임에 메모리 공간을 확보하고 메모리의 힙 영역에 저장됨.  
  
그래서, 객체 타입을 정의하려면 타입 이름, 프로퍼티나 메소드를 기술하는 함수를 하나 만들어야 함.  
이렇게 정의를 해 놓은 다음, 정의된 객체에도 새로운 속성을 추가할 수는 있지만, 다른 객체에는 영향을 주지 못함.  
새 속성을 해당 타입의 모든 객체에 다 추가하고 싶으면 그러면 어떻게 함?  
이때는 객체 타입의 정의에다가 추가를 해야하는거임 ㅇㅇ  
object.create 매서드를 이용하서도 객체를 생성할 수 있다. 이 매서드는 사용할 프로토타입 객체를 사용자가 직접 선택할 수 있음  
이게 뭔소리냐?  
자바스크립트의 모든 객체는 자신의 부모 역할을 담당하는 객체랑 연결되어 있음.  
이것은 (마치 객체지향의 상속 개념과 같이,) 부모 객체의 프로퍼티나 메소드를 상속받아 사용하는 것을 가능하게 함.  
이런 부모객체를 프로토타입 객체 또는 프로토타입이라고 함.    
즉, 부모객체를 선택할 수 있다는 것.    
상속?    
모든 객체는 최소 하나의 다른 객체로부터 상속을 받음.    
prototype이라는 생성자 객체에서 어떤게 상속되는지 알 수 있음.    
! 객체 프로퍼티의 인덱싱    
(이건 처음 안 내용인듯)    
객체 속성을 정의할 때의 방식에 따라서만 참조를 할수 있음.    
프로퍼티를 이름으로 정의->이름으로만 참조 가능    
인덱스를 이용하여 정의->인덱스를 이용해서만 참조 가능    
    
객체의 프로퍼티 정의    
prototype 프로퍼티를 이용해서, 미리 정의된 객체 타입에 속성을 추가할 수 있음.    
근데 이건 해당 객체 타입의 모든 인스턴스가 갖게 됨.    
ex) Car.prototype.color = null;    
    
  
