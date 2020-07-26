# 클래스 및 구조체(C# 프로그래밍 가이드)
원문 : https://docs.microsoft.com/ko-kr/dotnet/csharp/programming-guide/classes-and-structs/

## 캡슐화


## 멤버
C#에는 전역 변수 또는 메서드가 없다.

* 필드
* 상수
* 속성
* 메서드
* 생성자
* 이벤트
* 종료자
* 인덱서
* 연산자
* 중첩 형식

## 액세스 가능성
* public
* protected
* internal
* protected internal 
* **private(기본 액세스)**
* private protected


## 상속
* 클래스(구조체는 아님)는 상속 개념을 지원
* 파생클래스는 생성자와 종료자를 제외하고 기본 클래스의 모든 public, protected 및 internal 멤버를 자동으로 포함
* 메서드의 구현 강제하려면 abstract 선언
* 상속 못하게 하려면 sealed로 선언


