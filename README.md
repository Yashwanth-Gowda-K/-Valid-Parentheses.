📝 Problem Description

Given a string `s` containing just the characters `'('`, `')'`, `'{'`, `'}'`, `'['`, and `']'`, determine if the input string is valid.

A string is **valid** if:
1. Open brackets are closed by the same type of brackets.
2. Open brackets are closed in the correct order.
3. Every closing bracket has a corresponding opening bracket.

---

## 🧠 Approach

This problem is a classic application of the **stack** data structure. Here's how the algorithm works:

- Traverse each character in the string.
- If it's an **opening bracket**, push it onto the stack.
- If it's a **closing bracket**, check if it matches the top of the stack.
  - If it matches, pop the stack.
  - If it doesn't match or the stack is empty, return `False`.
- If the stack is empty at the end, return `True` (all brackets matched).

🧪 Example Test Cases
print(isValid("()"))        # True
print(isValid("()[]{}"))    # True
print(isValid("(]"))        # False
print(isValid("([)]"))      # False
print(isValid("{[]}"))      # True


🕰️ Time & Space Complexity
Time Complexity: O(n) — We iterate over the string once.

Space Complexity: O(n) — In the worst case, we push all characters onto the stack.
