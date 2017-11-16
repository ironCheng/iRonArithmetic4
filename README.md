# iRonArithmetic4
Arithmetic 4 / 算法题 4

##  荔枝笔试题

##  题目：数组a有n个元素，整数x在数组中出现的次数大于n>>1，求x。
##  要求：时间复杂度为O(n),空间复杂度为O(1) 

<pre><code>

int FindANumber(int *a, int length)
{
    int x = a[0];
    int times = 1;
    
    /* 遍历一次 */
    for (int i = 1; i < length; i++) {
        
        if (times == 0) {
            
            x = a[i];
            
        } else {
            /* 遇到相同的，times就加一 */
            if (x == a[i]) {
                
                times++;
            
            } else {
            
                times--;
            
            }   
        }
    }
    return x;
}
</code></pre>
