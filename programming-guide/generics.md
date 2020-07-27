# 제네릭(C# 프로그래밍 가이드)
* 원문 : https://docs.microsoft.com/ko-kr/dotnet/csharp/programming-guide/generics/
* 참고 : https://docs.microsoft.com/ko-kr/dotnet/standard/generics/
* 클래스 및 메서드를 인스턴스화 할때까지 하나 이상의 **형식지정을 지연** 하는 디자인 방법

```C#
// Declare the generic class.
public class GenericList<T>
{
    public void Add(T input) { }
}
class TestGenericList
{
    private class ExampleClass { }
    static void Main()
    {
        // Declare a list of type int.
        GenericList<int> list1 = new GenericList<int>();
        list1.Add(1);

        // Declare a list of type string.
        GenericList<string> list2 = new GenericList<string>();
        list2.Add("");

        // Declare a list of type ExampleClass.
        GenericList<ExampleClass> list3 = new GenericList<ExampleClass>();
        list3.Add(new ExampleClass());
    }
}
```

## Generic 개요
* 제네릭 형식을 사용하여 코드 재사용, 형식 안전성 및 성능을 최대화
* 일반적으로 제네릭은 컬렉션 클래스를 만드는 데 사용
* 용자 고유의 제네릭 인터페이스, 클래스, 메서드, 이벤트 및 대리자를 만들 수 있음
* 제네릭 데이터 형식에 사용되는 형식에 대한 정보는 리플렉션을 사용하여 런타임 시 얻을 수 있음

## 관련
* 제네릭 형식 매개 변수
* 형식 매개 변수에 대한 제약 조건
* 제네릭 클래스
* 제네릭 인터페이스
* 제네릭 메서드
* 제네릭 대리자
* C++ 템플릿과 C# 제네릭의 차이점
* 제네릭 및 리플렉션
* 런타임의 제네릭

