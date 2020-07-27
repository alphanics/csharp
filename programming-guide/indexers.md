# indexer
* 원문 : https://docs.microsoft.com/ko-kr/dotnet/csharp/indexers
* 인덱서는 속성과 비슷하다.
* 인덱서는 인덱싱된 속성이라고 생각하자.


## 인덱서 구문
```C#
var item = someObject["key"];
someObject["AnotherKey"] = item;
```

* this 키워드를 속성 이름으로 사용하고 대괄호 내에서 인수를 선언하여 인덱서를 선언
```C#
public int this[string key]
{
    get { return storage.Find(key); }
    set { storage.SetAt(key, value); }
}
```
