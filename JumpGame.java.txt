//problem:jump Game
//Dificulty: medium
//Runtime:1ms-Beats 99.95%
class Solution {
    public boolean canJump(int[] nums) {
        int n=nums.length;
        int LP=n-1;
        for(int i=n-2;i>=0;i--){
            if((i+nums[i])>=LP){
                LP=i;
            }
        }
        return LP==0;
    }
}