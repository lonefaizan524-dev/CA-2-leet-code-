CA3 DSA 

Q1 TWO SUM:
#include <vector>

class Solution
{
public:
    std::vector<int> twoSum(std::vector<int>& nums, int target)
    {
  
        for (int i = 0; i < nums.size(); i++)
        {
           
            for (int j = i + 1; j < nums.size(); j++)
            {
               
                if (nums[i] + nums[j] == target) 
                {
                    
                    return {i, j};
                }
            }
        }
      
        return {};
    }
};


Q2 PLUS ONES :
#include <vector>
class Solution {
public:
    std::vector<int> plusOne(std::vector<int>& digits)
    {
        int n = digits.size();
        
      
        for (int i = n - 1; i >= 0; i--)
        {
           
            if (digits[i] < 9)
            {
                digits[i] += 1;
                return digits;
            }
            
            
            digits[i] = 0;
        }
        
        digits.insert(digits.begin(), 1);
        
        return digits;
    }
};


Q3 MOVE ZEREOS:

#include <vector>

class Solution {
public:
    void moveZeroes(std::vector<int>& nums) {
        int insertPos = 0;
        
        
        for (int i = 0; i < nums.size(); i++) {
            if (nums[i] != 0) {
                nums[insertPos] = nums[i];
                insertPos++; 
            }
        }
        
     
        for (int i = insertPos; i < nums.size(); i++) {
            nums[i] = 0;
        }
    }
};
