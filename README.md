# CSharpbase

## 2023-02-02

### 예제로 배우는 C# 01

#### 기초 설명

- using + 시스템이라는 보따리
- using System.Collections.Generic < System이라는 보따리 안에 수많은 툴들이 들어있고 그중에서 Collection 안에 있는 Generic을 쓰겠음
- namespace : 만들 코드의 이름, 보따리를 만들어줌
- class Program < 역시 Program 안에 많은 툴이 들어가 있음
- static void Main(string[] args) < main이 메인으로 실행되는 함수, 그 안에 수많은 코딩이 들어감
- Console이라는 도화지에 무언가를 쓰겠다~무엇을? ex)Console.WriteLine("Hello World");
- Readkey(); < 키를 칠 때까지 창을 띄워놓는 명령어

args : 여러 개의 string을 가지고 있음
args.Length : string이 몇 개 넘어왔는지 알 수 있게 해줌
ex) Conosole.WriteLine(args.Length);
Console.WriteLine("Hello " + args[0]); * 제로부터 시작


#### 기초 설명 2

- bool (True/False)


#### 클래스의 데이터 전달 - 매개 변수, 멤버 변수
##### 매개 변수
##### 멤버 변수
public string Name


using System;

class Cat {
   public string Name;
   
  public Cat(string name) {
    Name = name;
    Console.WriteLine("고양이의 이름은 "+Name+"입니다.");
  }
}

class Program {
  public static void Main (String[] args) {
    Cat myCat = new cat("코코");
    myCat.Name = "몰리";
    Console.WriteLine("고양이의 이름은 "+myCat.Name+"입니다.");
    }
}

Console.WriteLine이라는 메소드를 통해서 매개변수로 Hello World라는 문자열을 전달했습니다.
Program이라는 메인클래스에서 Console이라는 클래스로 데이터 전달

멤버변수: Name이라는 멤버 변수를 만듬 > 그 값을 instance 변수로 만든 다음 > instance 변수에서 Name 변수 호출 > 이퀄 연산자로 값을 바꿈

ex)
using System;

class Cat {
  public string Name;
  
  public Cat(string name) {
    Name = name;
    Console.WriteLine("고양이의 이름은 "+Name+"입니다.");
    }
}


class MainClass {
  public static void Main (string[] args) {
    Cat coco = new Cat("코코");
    coco.Name = "몰리";
    Console.WriteLine("고양이의 이름은 "+coco.Name+"입니다.");
    }
}

고양이 이름을 코코에서 몰리로 변경 가능


원래 코코라는 이름으로 초기화했는데 변경하고 나서는 몰리가 될 것


#### 클래스의 데이터 전달 - private, this 키워드
외부 호출여부를 결정.
public > 외부에서 호출 가능
private > 불가. 내부에서만


this.name = name;'

set: 값 설정
get: 값 가져옴
SetName, GetName

ex)
using System;

class Cat {
  private string name;
  
  public Cat(string name) {
    this.name = name;
    Console.WriteLine("고양이의 이름은 "+Name+"입니다.");
    }
    
    public SetName(string name) {
      this.name = name; // this라는 연산자로 자기자신의 클래스를 나타내고 뒤에 있는 네임은 매개 변수로 입력받은 문자
    }
}


class MainClass {
  public static void Main (string[] args) {
    Cat ㅓㅐ
    = new Cat("코코");
    coco.Name = "몰리";
    Console.WriteLine("고양이의 이름은 "+coco.Name+"입니다.");
    }
}
