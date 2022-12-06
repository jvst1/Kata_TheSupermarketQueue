Equipe: Gustavo Bosco e João Vitor de Souza Tomio.

Escolha um dos exercícios na lista abaixo, resolva usado clean code e TDD. Publique a solução no GitHub ou GitLab.​

[The Supermarket Queue](https://www.codewars.com/kata/57b06f90e298a7b53d000a86)

#Solução:
```csharp
using System;
using System.Linq;

public class Kata
{
	public static long QueueTime(int[] customers, int n)
	{
		var checkers = Enumerable.Repeat(0, n).ToArray();
		foreach (var customer in customers)
		{
			checkers[0] += customer;
			Array.Sort(checkers);
		}
		return checkers.Max();
	}
}
```