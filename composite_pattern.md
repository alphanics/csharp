# 합성패턴( Composite pattern )

* 합성 패턴은 같은 인터페이스를 상속받은 클래스들을 일괄 처리하는 패턴

```C#
public interface INode
{
  void Print();
}

public class Node1 : INode
{
  public void Print()
  {
    Console.WriteLine("Node1");
  }
}
public class Node2 : INode
{
  public void Print()
  {
    Console.WriteLine("Node2");
  }
}
public class Node3 : INode
{
  public void Print()
  {
    Console.WriteLine("Node3");
  }
}

public class CompositeNode : List<INode>, INode
{
  public void Print()
  {
    foreach(var node in this)
    {
      node.Print();
    }
  }
}

class Program
{
  static void Main(string[] args)
  {
    var composite = new CompositeNode();
    composite.Add(new Node1());
    composite.Add(new Node2));
    composite.Add(new Node3));
    
    composite.Print();
  }
}
```























