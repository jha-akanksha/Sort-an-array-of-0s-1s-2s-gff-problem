# Sort-an-array-of-0s-1s-2s-gfg-problem
class Solution
{
    public static void sort012(int a[], int n)
    {
        // code here 
        int low=0;
        int mid=0;
        int high=n-1;
        
        while(mid<=high)
        {
            if( a[mid]==0)
            {
                int temp=a[low];
                a[low]=a[mid];
                a[mid]=temp;
                
                low++;
                mid++;
            }
            else if(a[mid]==2)
            {
               int temp=a[high];
                a[high]=a[mid];
                a[mid]=temp;  
                
                high--;
            }
            else mid++;
        }
    }
}
