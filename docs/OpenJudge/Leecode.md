
class Solution:
    def plusOne(self, digits: List[int]) -> List[int]:
        for i in range(len(digits) - 1, -1, -1):  # 从末尾往前遍历
            if digits[i] < 9:
                digits[i] += 1
                return digits  # 直接返回
            digits[i] = 0  # 进位
        return [1] + digits  # 处理全 9 的情况