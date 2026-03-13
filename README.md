15.Postfix Evaluation with User Input

def evaluate(exp):
    stack=[]

    for ch in exp:
        if ch.isdigit():
            stack.append(int(ch))
        else:
            b=stack.pop()
            a=stack.pop()

            if ch=='+':
                stack.append(a+b)
            elif ch=='-':
                stack.append(a-b)
            elif ch=='*':
                stack.append(a*b)
            elif ch=='/':
                stack.append(a/b)

    return stack.pop()

exp = raw_input("Enter Postfix Expression: ")

print("Result:", evaluate(exp))

Output:
Enter Postfix Expression: 82/3+
Result: 7
