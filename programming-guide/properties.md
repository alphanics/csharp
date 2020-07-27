# 속성
* 원문 : https://docs.microsoft.com/ko-kr/dotnet/csharp/properties
* 필드와 속성은 엄밀하게는 다른 것이나 구별할 필요는 없다.
* field는 storage, property는 setter, getter 접근자

```C#
public class Person   
{  
    private int Id; //Field  
    public int User_ID   
    {   
      //Property  
      get   
      {  
        return Id;  
      }  
      set   
      {  
        Id = value;  
      }  
    } 
}
```

## 속성구문
```C#
// field
public class Person
{
    public string FirstName;
}

// property default
public class Person
{
    public string FirstName { get; set; }
}

// property initialize
public class Person
{
    public string FirstName { get; set; } = string.Empty;
}

// property and field
public class Person
{
    public string FirstName
    {
        get { return firstName; }
        set { firstName = value; }
    }
    private string firstName;
}

// member => expression;
// https://www.c-sharpcorner.com/article/expression-bodied-members/
public class Person
{
    public string FirstName
    {
        get => firstName;
        set => firstName = value;
    }
    private string firstName;
}
```


## Validation
```C#
public class Person
{
    public string FirstName
    {
        get => firstName;
        set
        {
            if (string.IsNullOrWhiteSpace(value))
                throw new ArgumentException("First name must not be blank");
            firstName = value;
        }
    }
    private string firstName;
}
```

## Read-only
```C#
public class Person
{
    public string FirstName { get; private set; }
}

public class Person
{
    public Person(string firstName) => this.FirstName = firstName;
    public string FirstName { get; }
}
// 자주 사용하는 방법
public class Measurements
{
    public ICollection<DataPoint> points { get; } = new List<DataPoint>();
}
```

## Computed properties
```C#
public class Person
{
    public string FirstName { get; set; }
    public string LastName { get; set; }
    public string FullName { get { return $"{FirstName} {LastName}"; } }
}

public class Person
{
    public string FirstName { get; set; }
    public string LastName { get; set; }
    private string fullName;
    public string FullName
    {
        get
        {
            if (fullName == null)
                fullName = $"{FirstName} {LastName}";
            return fullName;
        }
    }
}

```

## Attaching attributes to auto-implemented properties
```C#
public class Person
{
    public string FirstName { get; set; }
    public string LastName { get; set; }
    [field:NonSerialized]
    public int Id { get; set; }
    public string FullName => $"{FirstName} {LastName}";
}
```


## Implementing INotifyPropertyChanged
```C#
public class Person : INotifyPropertyChanged
{
    public string FirstName
    {
        get => firstName;
        set
        {
            if (string.IsNullOrWhiteSpace(value))
                throw new ArgumentException("First name must not be blank");
            if (value != firstName)
            {
                PropertyChanged?.Invoke(this,
                    new PropertyChangedEventArgs(nameof(FirstName)));
            }
            firstName = value;
        }
    }
    private string firstName;
    public event PropertyChangedEventHandler PropertyChanged;
}
```

