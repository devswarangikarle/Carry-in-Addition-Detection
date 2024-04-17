# Carry-in-Addition-Detection
You're given two numbers A and B. On A+B, if there's a carry in this operation print "Yes" else "No". (Case specific) Input The input contains two space separated numbers: A, B  Constraints A and B are integers. 1 ≤ A, B ≤ 10^18 Output If the calculation does not involve a carry, print "No"; if it does, print "Yes".

def has_carry(A, B):
    carry = 0
    while A > 0 or B > 0:
        digit_A = A % 10
        digit_B = B % 10
        
        total = digit_A + digit_B + carry
        
        if total >= 10:
            return "Yes"
        
        carry = total // 10
        
        A //= 10
        B //= 10
    
    return "No"
A, B = map(int, input().strip().split())

print(has_carry(A, B))
