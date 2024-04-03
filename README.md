# First-Non-Repeating-Character in python
s = input()
count = [0] * 256
flag = 0
ch = ' '
for i in range(len(s)):
    count[ord(s[i])] += 1

for i in range(len(s)):
    if count[ord(s[i])] == 1:
        flag = 1
        ch = s[i]
        break

if flag == 1:
    print(ch)
else:
    print("All the characters are repetitive")
