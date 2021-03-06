# 객체지향 프로그래밍(Object Oriented Programming)

### 객체지향 프로그래밍(Object Oriented Programming)이란?

객체지향 프로그래밍, 줄여서 OOP란 `컴퓨터 프로그래밍 패러다임 중 하나로, 프로그램에 필요한 데이터를 추상화 시켜 상태와 행위를 가지는 객체를 만들고 그 객체들 간 유기적인 상호과정을 통해 로직을 구성하는 프로그래밍 방법`이다.



\* `객체(Object)` : 물리적으로 존재하거나 추상적으로 생각할 수 있는 것 중에서 자신의 속성을 가지고 있고 다른것과 식별 가능한 것. 객체는 속성과 동작으로 구성되어 있다고 보면 되는데 자바에서는 속성은 field, 동작은 method로 구현된다.



### 객체지향 프로그래밍의 장,단점

#### 장점

**1. 재사용성**
상속 등을 통해 프로그래밍시 코드의 재사용을 높일 수 있음.

**2. 생산성 향상**
잘 설계된 클래스를 만들어서 독립적인 객체를 사용함으로써 개발의 생산성을 향상시킬 수 있음. 

**3. 자연적인 모델링**
우리 일상생활의 모습의 구조가 객체에 자연스럽게 녹아들어 있기 때문에 생각하고 있는 것을 그대로 자연스럽게 구현할 수 있다. 

**4. 유지보수의 우수성**
프로그램 수정시 추가, 수정을 하더라도 캡슐화를 통해 주변 영향이 적기때문에 유지보수가 쉬워서 매우 경제적이라 할 수 있다.



#### 단점

**1. 개발속도가 느림**
객체가 처리하려는 것에 대한 정확한 이해가 필요하기에 설계단계부터 많은 시간이 소모 된다.

**2. 실행속도가 느림**
객체지향언어는 대체적으로 실행속도가 느리다. 

**3. 코딩난이도 상승**
설계 시 많은 시간과 노력이 든다. 다중 상속이 지원되는 C++ 같은 경우에 너무 복잡해져 코딩의 난이도가 상승할 수 있다.



### 객체지향프로그래밍의 특징

#### 1. 추상화(Abstraction)

>어떤 영역에서 필요로 하는 속성이나 행동을 추출하는 작업

OOP에서 말하는 객체는 실제 세계에 존재하는 대상을 프로그램에 필요한 데이터를 모델링한 것이다. 이 때 객체를 모델링하기 위해서는 객체의 특징을 잘 반영해야할 것이다. 마우스를 예로 들어보자. 실제 세계에 존재하는 마우스들의 모양, 색, 무게 등의 형태는 제각각이지만 마우스라면 지녀야할 특징들이 있다. 왼쪽 버튼, 오른쪽 버튼, 스트롤 휠 등은 마우스라면 필요한 요소들이다. 이렇게 **추상화는 상세한 정보는 무시하고 필요성에 의해 있어야할 정보들만 간추려서 구성하는 것**을 의미한다. 공통적으로 가질 수 있는 정보들을 추상화한다고 하며 프로그래밍의 세계로 접근, 접목 시킨 것이 객체지향 프로그래밍에서의 추상화이다.



#### 2. 캡슐화(Encapsulation)

> 데이터와 코드의 형태를 외부로부터 알 수없게 하고, 데이터의 구조와 역할, 기능을 하나의 캡슐형태로 만드는 방법
>
> ''데이터(field)''와 ''데이터를 다루는 방법(method)''을 하나로 묶는 것

캡슐화는 데이터 구조와 데이터를 다루는 방법을 하나로 묶는 것이다. 하지만 그렇다고 무작정 묶으면 되는 것이 아니라 객체가 맡은 역할을 수행하기 위한 하나의 목적을 한데 묶는다고 생각해야한다. 그리고 이러한 캡슐화는 내부의 정보를 외부에 보이지 않도록 한다. 캡슐화라는 특징 덕분에 객체 내부가 어떤 형태로 구성되어 있는지 몰라도 원하는 결과를 얻을 수 있다. (우리는 String 타입에 대해 replace()함수를 구체적으로 어떻게 구현되었는지 몰라도 사용가능하다.)



#### 3. 상속(Inheritance)

> 상위 클래스의 모든걸 하위 클래스가 모두 이어 받는 것. 즉, 부모가 자식에게 유전자를 물려주듯이 부모의 특징을 자식에게 모두 물려준다.

상속은 하나의 객체에 정의된 코드를 다른 객체에게 이어받을 수 있도록 하는 것이다. 예를 들어 Animal이라는 클래스를 하나 만들고 속성으로 울음소리(sound)를 가진다고 하자. 모든 동물은 울음소리라는 공통적인 특징이 있지만 구체적인 울음 소리는 다를 것이다. 상속의 개념이 없다면 같은 특징이라도 하나하나 구현을 해야겠지만, Animal이라는 상위 클래스를 상속 받고 동물마다 각각의 울음소리로만 바꿔준다면 코드의 중복성을 줄이고 재사용성을 높이게 된다는 강점을 갖는다.



#### 4. 다형성(Polymorphism)

> '하나의 객체가 여러가지 형태를 가질 수 있는 능력'을 의미. 

자바에서는 한 타입의 참조변수로 여러 타입의 객체를 참조할 수 있도록 한다. 코드 측면에서 보면 다형성은 하나의 타입에 여러 객체를 대입함으로써 다양한 기능을 이용할 수 있으며 객체를 부품화하여 유지 보수를 용이하게 한다. 예를 들어 Animal이라는 클래스를 만들고 이를 상속받은 Tiger, Lion 클래스가 있다고 하자. 동물 객체를 파라미터로 받아 울음소리를 출력하는 메소드 bark()를 구현한다고 할 때 다형성이 없다면 다음과 같이 구현될 것이다.

```java
// Tiger tiger = new Tiger();
// Lion lion = new Lion();

public void bark(Tiger tiger) {
  System.out.println(tiger.sound);
}

public void bark(Lion lion) {
  System.out.println(lion.sound);
}
```

다형성을 적용한다면 다음과 같이 간단하게 구현 가능하다.

```java
// Animal tiger = new Tiger();
// Animal lion = new Lion();

public void bark(Animal animal) {
  System.out.println(animal.sound);
}
```





### OOP 관련 이슈

#### 1. getter와 setter를 사용하는 이유?

객체 내의 필드들을 private으로 선언하여 외부에서 필드에 직접 접근하지 못하도록 하고, getter와 setter 메소드로만 접근할 수 있도록 해논 이유가 무엇일까? 그것은 바로 **데이터의 무결성**을 위해서라고 한다. 예를 들어 Man이라는 클래스에 weight(몸무게)라는 필드가 존재한다고 하자. weight는 0보다 작을 수 없기 때문에 음수의 값이 들어오는 것을 방지해야한다. 만약, 필드에 직접 접근이 가능하다면 weight의 값은 외부에서 들어오는 값을 전혀 필터링하지 않고 변경이된다. 반대로 setter메소드를 이용한다면 외부로부터 파라미터로 입력받은 값에 대해 유효성을 체크할 수 있게 된다. 





### [참고]

> - [Java - (5) 객체란? 객체 지향 프로그래밍의 특징]( https://jwprogramming.tistory.com/121)
> - [객체 지향 프로그래밍이 뭔가요? (꼬리에 꼬리를 무는 질문 1순위, 그놈의 OOP)](https://jeong-pro.tistory.com/95)
> - [Getter, Setter를 사용하는 이유](https://thiago6.tistory.com/75)
> - [객체 지향 프로그래밍의 추상화](https://webclub.tistory.com/137)
> - [객체지향 언어의 특징 : 추상화 은닉화 캡슐화](https://halfmoon9.tistory.com/62)
> - [다형성](https://wikidocs.net/269)