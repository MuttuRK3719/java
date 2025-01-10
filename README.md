class Solution {
    long maxProduct(int[] arr) {
        Arrays.sort(arr);  // Sort the array
        
        int n = arr.length;
        
        // Product of the three largest numbers
        long product1 = (long) arr[n - 1] * arr[n - 2] * arr[n - 3];
        
        // Product of two smallest numbers and the largest number
        long product2 = (long) arr[0] * arr[1] * arr[n - 1];
        
        return Math.max(product1, product2);
    }
}
