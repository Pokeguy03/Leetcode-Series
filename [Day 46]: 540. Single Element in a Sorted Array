# With Binary_search
class Solution:
    def singleNonDuplicate(self, nums: List[int]) -> int:
        if len(nums)==1:
            return nums[0]
        if nums[0]!=nums[1]:
            return nums[0]
        if nums[-1]!=nums[-2]:
            return nums[-1]
        left=0
        right=len(nums)-1
        while left<=right:
            mid=(left+right)//2
            if nums[mid]!=nums[mid-1] and nums[mid]!=nums[mid+1]:
                return nums[mid]
            elif((mid%2==1) and (nums[mid-1]==nums[mid])) or ((mid%2==0) and (nums[mid]==nums[mid+1])):
                left=mid+1
            else:
                right=mid-1
        return -1
      
  #Without Binary_Search
        s=Counter(nums)
        for i in range(len(nums)):
            if s[nums[i]]==1:
                return nums[i]
