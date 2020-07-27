# XML 주석을 사용하여 코드 문서화
* 원문 : https://docs.microsoft.com/ko-kr/dotnet/csharp/codedoc
*  .csproj 프로젝트 파일의 <PropertyGroup> 섹션에 GenerateDocumentationFile 요소 추가
```XML
<GenerateDocumentationFile>true</GenerateDocumentationFile>

<DocumentationFile>bin\$(Configuration)\$(TargetFramework)\$(AssemblyName).xml</DocumentationFile>
```

* XML 문서 주석에는 삼중 슬래시(///) 및 XML 형식의 주석 본문이 사용
```C#
/// <summary>
/// This class does something.
/// </summary>
public class SomeClass
{
}
```

## 연습

### \<summary\>

### \<remarks\>

### \<returns\>

### \<value\>

### \<example\>

### \<para\>

### \<c\>

### \<exception\>

### \<see\>

### \<seealso\>

### \<param\>

### \<typeparam\>

### \<paramref\>

### \<typeparamref\>

### \<list\>

### \<inheritdoc\>

### \<include\>

## 사용자 정의 태그

## 권장사항
* 일관성 보장
* IntelliSense에는 <summary> 태그의 내용이 필요함
* 컴파일러에서 <exception>, <include>, <param>, <see>, <seealso> 및 <typeparam> 태그 구문 확인함.

## 참조
* XML 문서 주석(C# 프로그래밍 가이드)(https://docs.microsoft.com/ko-kr/dotnet/csharp/programming-guide/xmldoc/)
* 문서 주석에 대한 권장 태그(C# 프로그래밍 가이드)(https://docs.microsoft.com/ko-kr/dotnet/csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments)
