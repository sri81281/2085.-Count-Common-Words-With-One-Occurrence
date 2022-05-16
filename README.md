# 2085.-Count-Common-Words-With-One-Occurrence

Input: words1 = ["leetcode","is","amazing","as","is"], words2 = ["amazing","leetcode","is"] Output: 2

Input: words1 = ["b","bb","bbb"], words2 = ["a","aa","aaa"]
Output: 0
Explanation: There are no strings that appear in each of the two arrays.


Input: words1 = ["a","ab"], words2 = ["a","a","a","ab"]
Output: 1
Explanation: The only string that appears exactly once in each of the two arrays is "ab".


class Solution {
    public int countWords(String[] words1, String[] words2) {
        int count=0;
        int result=0;
        if(words1.length>=words2.length){
        for(int i=0;i<words2.length;i++)
        {
            count=0;
            for(int j=0;j<words1.length;j++)
            {
                if(words2[i].equals(words1[j]))
                {
                    count+=1;
                }
            }
            if(count==1)
            {
                result++;
            }
        }
        }
        else
        {
            for(int i=0;i<words1.length;i++)
        {
              count=0;
            for(int j=0;j<words2.length;j++)
            {
                if(words1[i].equals(words2[j]))
                {
                    count+=1;
                }
            }
            if(count==1)
            {
                result++;
            }
        }
        }
         return result;  
        }   
}

