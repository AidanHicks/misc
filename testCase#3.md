```cs

//Create array of nums 36 - 180
int size = 144;
int start = 36;

int count = 0;

int[] nums = new int[size];

for (int i = 0; i < nums.Length; i++)
{
    nums[i] = start;
    start++;
}

//Begin loop to evaluate tip, top and tap

for (int i = 0; i < nums.Length; i++)
{
    bool tip = false;
    bool top = false;
    bool tap = false;

    if (nums[i] % 2 == 0)
    {
        tip = true;
    }
    if (nums[i] % 6 == 0)
    {
        top = true;
    }

    string temp = nums[i].ToString();

    int total = 0;

    for (int j = 0; j < temp.Length; j++)
    {
        int tempNum = (int)temp[j] - '0';

        total += tempNum;

    }

    if (total % 2 != 0)
    {
        tap = true; 
    }

    if (tip && top && tap)
    {
        count++;
    }

    Console.WriteLine($"Iteration{i + 36}: tip={tip} top ={top} tap = {tap} and count = {count}");

}

Console.WriteLine(count);
Console.ReadLine();

```
