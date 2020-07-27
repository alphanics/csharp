# 형식(types)

## 형식에 저장된 정보
* 형식 변수에 필요한 스토리지 공간.
* 형식이 나타낼 수 있는 최대값 및 최소값.
* 형식에 포함되는 멤버(메서드, 필드, 이벤트 등).
* 형식이 상속하는 기본 형식.
* 런타임에 변수에 대한 메모리가 할당될 위치.
* 허용되는 작업 유형.

-. 컴파일러는 형식 정보를 실행 파일에 메타데이터로 포함한다.
-. CLR(공용 언어 런타임)는 런타임에 이 메타데이터를 사용하여 메모리를 할당 및 회수할 때 형식 안정성을 추가로 보장.

## 기본 제공 형식
기본값 형식
* 정수
* 부동소수점
* bool
* char
* 열거형
* 구조체
* 튜플
* Nullable

|C# 형식 키워드|	.NET 형식|
|------------------|------------------|
|bool|	System.Boolean|
|byte|	System.Byte|
|sbyte|	System.SByte|
|char|	System.Char|
|decimal|	System.Decimal|
|double|	System.Double|
|float|	System.Single|
|int|	System.Int32|
|uint|	System.UInt32|
|long|	System.Int64|
|ulong|	System.UInt64|
|short|	System.Int16|
|ushort|	System.UInt16|

참조형식
* class
* interface
* nullable

|C# 형식 키워드|	.NET 형식|
|------------------|------------------|
|object|	System.Object|
|string|	System.String|
|dynamic|	System.Object|

