## Data Structures, Algorithms and Complexity Homework

1. 
**What is the expected running time of the following C# code?**
  
	- Explain why using Markdown.
  
	- Assume the array's size is `n`.

```cs  
long Compute(int[] arr)
{
    long count = 0;
    for (int i=0; i<arr.Length; i++)
    {
        int start = 0, end = arr.Length-1;
        while (start < end)
            if (arr[start] < arr[end])
                { start++; count++; }
            else 
                end--;
    }
	return count;
}
```

Answer: The complexity of the code would be 0(n ^ 2) 



2. **What is the expected running time of the following C# code?**
  
	-Explain why using Markdown.
  
	- Assume the input matrix has size of `n * m`.

```cs   
long CalcCount(int[,] matrix)
{
    long count = 0;
    for (int row=0; row<matrix.GetLength(0); row++)
        if (matrix[row, 0] % 2 == 0)
            for (int col=0; col<matrix.GetLength(1); col++)
                if (matrix[row,col] > 0)
                    count++;
    return count;
}
```

Answer: The complexity of the code would be 0(n * m)
