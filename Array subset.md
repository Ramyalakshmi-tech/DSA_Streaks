class Solution {
    public boolean isSubset(int a[], int b[]) {
        // Your code here
        Arrays.sort(a);
        Arrays.sort(b);
        int j=0;
        int i=0;
        while(i<a.length && j<b.length){
            if(a[i]==b[j]){
                i++;
                j++;
            }
            else if(a[i]>b[j]){
                return false;
            }
            else
                i++;
        }
        
        
        return j==b.length;
    }
}
