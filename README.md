# 9._Palindrome_Number
# Given an integer x, return true if x is a palindrome, and false otherwise.
class Solution {
public:
    bool isPalindrome(int x){
        if(x<0) return false; // Negative numbers cannot be palindromes
        int original=x;
        int sum=0;
        while(x>0){
            if(sum>INT_MAX/10) return false; // Check for integer overflow before multiplying
            sum=sum*10+(x%10);
            x=x/10;
        }
        return sum==original;
    }
};
