{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# Mastering Python Basics: My CodingBat Journey 🐍\n",
    "\n",
    "## By Aditya\n",
    "\n",
    "Welcome to my journey through the fundamentals of Python programming! As I delve deeper into Python, I've found CodingBat to be an excellent platform for honing my problem-solving skills and understanding core concepts. This post compiles my solutions, offering not just the code, but also a brief explanation of the logic behind each one. I hope this helps others who are on a similar learning path!"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Warmup-1: Getting Started with Python Logic\n",
    "\n",
    "This section focuses on basic logic and conditional statements."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `sleep_in`\n",
    "\n",
    "**Question:** The parameter `weekday` is `True` if it is a weekday, and the parameter `vacation` is `True` if we are on vacation. We sleep in if it is not a weekday or we're on vacation. Return `True` if we sleep in."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def sleep_in(weekday, vacation):\n",
    "  return (not weekday) or (vacation)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** We sleep in if it's `NOT` a `weekday` OR if we `are on vacation`. This directly translates to the boolean logic `(not weekday) or vacation`."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `monkey_trouble`\n",
    "\n",
    "**Question:** We have two monkeys, a and b, and the parameters `a_smile` and `b_smile` indicate if each is smiling. We are in trouble if they are both smiling or if neither of them is smiling. Return `True` if we are in trouble."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def monkey_trouble(a_smile, b_smile):\n",
    "  return a_smile==b_smile"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** We are in trouble if their smiling states are the same. If `a_smile` is `True` and `b_smile` is `True`, they are the same. If `a_smile` is `False` and `b_smile` is `False`, they are also the same. The `==` operator elegantly captures both conditions."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `sum_double`\n",
    "\n",
    "**Question:** Given two int values, return their sum. Unless the two values are the same, then return double their sum."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def sum_double(a, b):\n",
    "  return 2*(a+b) if a==b else a+b"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** This uses a Pythonic conditional expression (ternary operator). If `a` equals `b`, we return `2 * (a + b)`; otherwise, we return their simple sum `a + b`."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `diff21`\n",
    "\n",
    "**Question:** Given an int `n`, return the absolute difference between `n` and 21, except return double the absolute difference if `n` is over 21."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def diff21(n):\n",
    "  return abs(n-21)*2 if n>21 else abs(n-21) "
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** Similar to `sum_double`, a conditional expression checks if `n` is greater than 21. If so, we double the absolute difference; otherwise, we just return the absolute difference. `abs()` ensures a positive result."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `parrot_trouble`\n",
    "\n",
    "**Question:** We have a loud talking parrot. The \"hour\" parameter is the current hour time in the range 0..23. We are in trouble if the parrot is talking and the hour is before 7 or after 20. Return `True` if we are in trouble."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def parrot_trouble(talking, hour):\n",
    "  return (talking and (hour < 7 or hour > 20))"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** We are in trouble only if the parrot `talking` is `True` AND (the `hour` is less than 7 OR the `hour` is greater than 20). The parentheses clearly group the hour conditions."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `makes10`\n",
    "\n",
    "**Question:** Given 2 ints, `a` and `b`, return `True` if one of them is 10 or if their sum is 10."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def makes10(a, b):\n",
    "  return (a == 10 or b == 10 or a+b == 10) "
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** This is a straightforward application of the `or` operator. If any of the three conditions (`a` is 10, `b` is 10, or their sum is 10) are true, the function returns `True`."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `near_hundred`\n",
    "\n",
    "**Question:** Given an int `n`, return `True` if it is within 10 of 100 or 200. Note: `abs(num)` computes the absolute value of a number."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def near_hundred(n):\n",
    "  return (abs(n-100) <=10 ) or (abs(n-200) <=10 )"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** We check if the absolute difference between `n` and 100 is 10 or less, OR if the absolute difference between `n` and 200 is 10 or less. `abs()` ensures a positive result."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `pos_neg`\n",
    "\n",
    "**Question:** Given 2 int values, return `True` if one is negative and one is positive. Except if the parameter \"negative\" is `True`, then return `True` only if both are negative."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def pos_neg(a, b, negative):\n",
    "  if negative:\n",
    "    if a<0 and b<0:\n",
    "      return True\n",
    "    else:\n",
    "      return False\n",
    "  elif (a<0 and b>0) or (a>0 and b<0):\n",
    "    return True\n",
    "  else:\n",
    "    return False\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** This uses an `if-elif-else` structure to handle the two main cases.\n",
    "* If `negative` is `True`, we specifically check if both `a` and `b` are negative.\n",
    "* Otherwise (if `negative` is `False`), we check if one is negative AND the other is positive."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `not_string`\n",
    "\n",
    "**Question:** Given a string, return a new string where \"not \" has been added to the front. However, if the string already begins with \"not\", return the string unchanged."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def not_string(str):\n",
    "  return \"not \"+str if not str.startswith(\"not\") else str"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** A conditional expression checks if the string `str_val` starts with \"not\" using `str_val.startswith(\"not\")`. If it doesn't, we prepend \"not \"; otherwise, we return the original string."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `missing_char`\n",
    "\n",
    "**Question:** Given a non-empty string and an int `n`, return a new string where the char at index `n` has been removed. The value of `n` will be a valid index of a char in the original string (i.e. `n` will be in the range 0..len(str)-1 inclusive)."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def missing_char(str, n):\n",
    "  return str.replace(str[n],\"\") "
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** This uses the `str.replace()` method. It attempts to replace all occurrences of the character at index `n` with an empty string. While this works for unique characters, it might have unintended side effects if the character at `n` appears multiple times in the string."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `front_back`\n",
    "\n",
    "**Question:** Given a string, return a new string where the first and last chars have been exchanged."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def front_back(str):\n",
    "  return str[-1] + str[1:-1] + str[0] if len(str) >1 else str"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** If the string length is greater than 1, we construct the new string by taking the last character (`str_val[-1]`), then the middle part (`str_val[1:-1]`), and finally the first character (`str_val[0]`). If the string is length 0 or 1, we return it unchanged."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `front3`\n",
    "\n",
    "**Question:** Given a string, we'll say that the front is the first 3 chars of the string. If the string length is less than 3, the front is whatever is there. Return a new string which is 3 copies of the front."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def front3(str):\n",
    "  return str if str == \"\" else str[:3]*3"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** This solution first checks if the string is empty. If so, it returns an empty string. Otherwise, it takes the first 3 characters (or fewer if the string is shorter) using slicing `[:3]` and repeats them three times using the `*` operator."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Warmup-2: Looping and Array Basics\n",
    "\n",
    "This section introduces more complex string and list manipulations, often involving loops."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `string_times`\n",
    "\n",
    "**Question:** Given a string and a non-negative int `n`, return a larger string that is `n` copies of the original string."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def string_times(str, n):\n",
    "  return str*n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** Python's string multiplication `*` operator directly handles this. Multiplying a string by an integer `n` repeats the string `n` times."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `front_times`\n",
    "\n",
    "**Question:** Given a string and a non-negative int `n`, we'll say that the front of the string is the first 3 chars, or whatever is there if the string is less than length 3. Return `n` copies of the front;"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def front_times(str, n):\n",
    "  return str[:3]*n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** Similar to `front3` and `string_times`, we combine string slicing `[:3]` (which gets the first 3 chars or fewer if the string is shorter) with string multiplication `* n`."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `string_bits`\n",
    "\n",
    "**Question:** Given a string, return a new string made of every other char starting with the first, so \"Hello\" yields \"Hlo\"."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def string_bits(str):\n",
    "  return str[::2]"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** This is a classic use case for extended slicing in Python. `str_val[start:stop:step]` with a `step` of 2 means \"take every second character from the beginning to the end\"."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `string_splosion`\n",
    "\n",
    "**Question:** Given a non-empty string like \"Code\" return a string like \"CCoCodCode\"."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def string_splosion(str):\n",
    "  ans_string = \"\"\n",
    "  i=0\n",
    "  while(i<=len(str)):\n",
    "    ans_string += str[:i]\n",
    "    i += 1\n",
    "  return ans_string"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** We initialize an empty `ans_string`. We then use a `while` loop that iterates from `i=0` up to and including the length of the string. In each iteration, we append a slice of the original string from the beginning up to the current index `i` (`str_val[:i]`)."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `last2`\n",
    "\n",
    "**Question:** Given a string, return the count of the number of times that a substring length 2 appears in the string and also as the last 2 chars of the string, so \"hixxxhi\" yields 1 (we won't count the end substring)."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def last2(str):\n",
    "  if len(str) <=2:\n",
    "    return 0\n",
    "  else:\n",
    "    ending_2_characters = str[-2:]\n",
    "    count = 0\n",
    "    for i in range(len(str)-2):\n",
    "      if ending_2_characters == str[i]+str[i+1]:\n",
    "        count += 1\n",
    "    return count"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:**\n",
    "1.  Handle short strings: If the string is less than 2 characters, no 2-char substring can exist, so return 0.\n",
    "2.  Get the target: Extract the last two characters of the string.\n",
    "3.  Iterate and compare: Loop through the string, stopping two characters before the end (`len(str_val) - 2`) to ensure we don't compare the ending substring with itself. In each iteration, check if the current 2-character slice matches the `ending_2_characters`."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `array_count9`\n",
    "\n",
    "**Question:** Given an array of ints, return the number of 9's in the array."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def array_count9(nums):\n",
    "  count = 0\n",
    "  for i in nums:\n",
    "    if i==9:\n",
    "      count += 1\n",
    "  return count"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** This code iterates through each number in the input list `nums`. If a number is equal to 9, a `count` variable is incremented. Finally, the total `count` of 9s is returned."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `array_front9`\n",
    "\n",
    "**Question:** Given an array of ints, return `True` if one of the first 4 elements in the array is a 9. The array length may be less than 4."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def array_front9(nums):\n",
    "  return 9 in nums[:4]"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** Python's slicing `nums[:4]` safely gets the first 4 elements (or fewer if the list is shorter). We then use the `in` operator to check directly if `9` exists within that slice. This is very clean and efficient."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `array123`\n",
    "\n",
    "**Question:** Given an array of ints, return `True` if the sequence of numbers 1, 2, 3 appears in the array somewhere."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def array123(nums):\n",
    "  for i in range(len(nums)-2):\n",
    "    if nums[i]==1 and nums[i+1] == 2 and nums[i+2] ==3:\n",
    "      return True\n",
    "      break;\n",
    "    \n",
    "  return False"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** We loop through the array, checking for a subsequence of `1, 2, 3` at each possible starting position `i`. The loop range `len(nums) - 2` ensures we don't go out of bounds when checking `nums[i+2]`."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `string_match`\n",
    "\n",
    "**Question:** Given 2 strings, `a` and `b`, return the number of the positions where they contain the same length 2 substring. So \"xxcaazz\" and \"xxbaaz\" yields 3, since the \"xx\", \"aa\", and \"az\" substrings appear in the same place in both strings."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def string_match(a, b):\n",
    "  count = 0\n",
    "  \n",
    "  if len(a) <=1 or len(b)<=1:\n",
    "    return count\n",
    "  \n",
    "  for i in range(min(len(a),len(b))-1):\n",
    "    if a[i:i+2] == b[i:i+2]  :\n",
    "      count += 1\n",
    "\n",
    "  return count"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** We find the minimum length of the two strings to ensure we don't go out of bounds. Then, we loop from the beginning up to `min_len - 1` (since we need to check two characters `i` and `i+1`). In each iteration, we compare the 2-character slices from both strings."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## String-1: String Manipulation\n",
    "\n",
    "This section covers common string operations."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `hello_name`\n",
    "\n",
    "**Question:** Given a string `name`, e.g. \"Bob\", return a greeting of the form \"Hello Bob!\"."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def hello_name(name):\n",
    "  return \"Hello \" + name + \"!\""
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** Simple string concatenation using the `+` operator."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `make_abba`\n",
    "\n",
    "**Question:** Given two strings, `a` and `b`, return the result of putting them together in the order abba, e.g. \"Hi\" and \"Bye\" returns \"HiByeByeHi\"."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def make_abba(a, b):\n",
    "  return a+b+b+a"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** Direct string concatenation in the specified `abba` order."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `make_tags`\n",
    "\n",
    "**Question:** The web is built with HTML strings like \"<i>Yay</i>\" which draws Yay as italic text. In this example, the \"i\" tag makes `<i>` and `</i>` which surround the word \"Yay\". Given `tag` and `word` strings, create the HTML string with tags around the word, e.g. \"<i>Yay</i>\"."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def make_tags(tag, word):\n",
    "  return \"<{0}>{1}</{0}>\".format(tag, word)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** Uses Python's `.format()` method for string formatting. The tag is used twice, once for the opening tag and once for the closing tag (with a `/`). `\"{0}\"` and `\"{1}\"` are placeholders for the `tag` and `word` respectively."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `make_out_word`\n",
    "\n",
    "**Question:** Given an \"out\" string length 4, such as \"<<>>\", and a word, return a new string where the word is in the middle of the out string, e.g. \"<<word>>\"."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def make_out_word(out, word):\n",
    "  return out[:2] + word + out[2:]"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** We take the first two characters of the `out` string (`out[:2]`), concatenate the `word`, and then concatenate the last two characters of the `out` string (`out[2:]`)."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `extra_end`\n",
    "\n",
    "**Question:** Given a string, return a new string made of 3 copies of the last 2 chars of the original string. The string length will be at least 2."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def extra_end(str):\n",
    "  return str[-2:]*3\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** We use slicing `[-2:]` to get the last two characters of the string, and then multiply that substring by 3."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `first_two`\n",
    "\n",
    "**Question:** Given a string, return the string made of its first two chars, so the String \"Hello\" yields \"He\". If the string is shorter than length 2, return whatever there is, so \"X\" yields \"X\", and the empty string \"\" yields the empty string \"\"."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def first_two(str):\n",
    "  return str[:2]"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** Python's string slicing `[:2]` is safe and concise. If the string is shorter than 2 characters, it will simply return the entire string without error (e.g., `\"\"[:2]` is `\"\"`, `\"X\"[:2]` is `\"X\"`)."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `first_half`\n",
    "\n",
    "**Question:** Given a string of even length, return the first half. So the string \"WooHoo\" yields \"Woo\"."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def first_half(str):\n",
    "  return str[:len(str)/2]"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** We calculate the length of the string, divide it by 2 using standard division (`/`), and then slice the string from the beginning up to that midpoint. Note that standard division (`/`) in Python 3 returns a float, which might cause issues if the slice index must be an integer. Integer division (`//`) would be safer here."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `without_end`\n",
    "\n",
    "**Question:** Given a string, return a version without the first and last char, so \"Hello\" yields \"ell\". The string length will be at least 2."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def without_end(str):\n",
    "  return str[1:-1]"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** Slicing from index 1 (skipping the first character) up to, but not including, the last character (`-1`) achieves this."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `combo_string`\n",
    "\n",
    "**Question:** Given 2 strings, `a` and `b`, return a string of the form short+long+short, with the shorter string on the outside and the longer string on the inside. The strings will not be the same length, but they may be empty (length 0)."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def combo_string(a, b):\n",
    "  return a+b+a if len(a)<len(b) else b+a+b"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** We compare the lengths of `a` and `b`. If `a` is shorter, we return `a + b + a`. Otherwise (meaning `b` is shorter, since they are guaranteed not to be the same length), we return `b + a + b`."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `non_start`\n",
    "\n",
    "**Question:** Given 2 strings, return their concatenation, except omit the first char of each. The strings will be at least length 1."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def non_start(a, b):\n",
    "  return a[1:]+b[1:]"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** We take slices of both strings starting from the second character (index 1) to the end (`[1:]`), and then concatenate them."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `left2`\n",
    "\n",
    "**Question:** Given a string, return a \"rotated left 2\" version where the first 2 chars are moved to the end. The string length will be at least 2."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def left2(str):\n",
    "  return str if len(str)<=2 else str[2:]+str[:2]"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** This solution first checks if the string length is 2 or less. If so, it returns the original string. Otherwise, it takes the slice from index 2 to the end (`str_val[2:]`) and concatenates it with the first two characters (`str_val[:2]`)."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## List-1: Basic List Operations\n",
    "\n",
    "This section focuses on fundamental list manipulations."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `first_last6`\n",
    "\n",
    "**Question:** Given an array of ints, return `True` if 6 appears as either the first or last element in the array. The array will be length 1 or more."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def first_last6(nums):\n",
    "  return True if nums[0] == 6 or nums[-1] == 6 else False"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** We directly check if the first element (`nums[0]`) is 6 OR if the last element (`nums[-1]`) is 6. The `True if ... else False` structure can be simplified to just the boolean expression itself."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `same_first_last`\n",
    "\n",
    "**Question:** Given an array of ints, return `True` if the array is length 1 or more, and the first element and the last element are equal."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def same_first_last(nums):\n",
    "  return True if len(nums) > 0 and nums[0]==nums[-1] else False"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** We first ensure the list has at least one element (`len(nums) > 0`) to prevent an `IndexError` when accessing `nums[0]` or `nums[-1]`. Then, we check if the first and last elements are equal. The `True if ... else False` structure can be simplified to just the boolean expression itself."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `make_pi`\n",
    "\n",
    "**Question:** Return an int array length 3 containing the first 3 digits of pi, {3, 1, 4}."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def make_pi():\n",
    "  return [3,1,4]"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** A direct return of the specified list."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `common_end`\n",
    "\n",
    "**Question:** Given 2 arrays of ints, `a` and `b`, return `True` if they have the same first element or they have the same last element. Both arrays will be length 1 or more."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def common_end(a, b):\n",
    "  return a[0] == b[0] if len(a) == 1 or len(b) == 1 else (a[0] == b[0])or(a[-1] == b[-1])"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** This solution checks if either array has a length of 1. If so, it only compares the first elements. Otherwise, it compares both the first elements AND the last elements. A simpler approach would be to directly use `(a[0] == b[0]) or (a[-1] == b[-1])` as the problem guarantees length 1 or more, making the `len` checks redundant."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `sum3`\n",
    "\n",
    "**Question:** Given an array of ints length 3, return the sum of all the elements."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def sum3(nums):\n",
    "  return nums[0]+nums[1]+nums[2]"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** This directly sums the three elements of the array by accessing them via their indices. Python's built-in `sum(nums)` function would also achieve the same result more concisely."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `rotate_left3`\n",
    "\n",
    "**Question:** Given an array of ints length 3, return an array with the elements \"rotated left\" so {1, 2, 3} yields {2, 3, 1}."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def rotate_left3(nums):\n",
    "  return nums[1:]+nums[:1]"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** We take a slice from the second element to the end (`nums[1:]`) and concatenate it with a slice containing only the first element (`nums[:1]`). This effectively moves the first element to the end."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `reverse3`\n",
    "\n",
    "**Question:** Given an array of ints length 3, return a new array with the elements in reverse order, so {1, 2, 3} becomes {3, 2, 1}."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def reverse3(nums):\n",
    "  return nums[::-1]"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** This uses advanced slicing `[start:stop:step]` with a step of `-1`. This creates a reversed copy of the list."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `max_end3`\n",
    "\n",
    "**Question:** Given an array of ints length 3, figure out which is larger, the first or last element in the array, and set all the other elements to be that value. Return the changed array."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def max_end3(nums):\n",
    "  return [max(nums[0],nums[-1])]*3\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** We find the maximum between the first and last elements using `max()`. Then, we create a new list where all three elements are set to this `max_val` by multiplying a single-element list by 3."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `sum2`\n",
    "\n",
    "**Question:** Given an array of ints, return the sum of the first 2 elements in the array. If the array length is less than 2, just sum up the elements that exist, returning 0 if the array is length 0."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def sum2(nums):\n",
    "  return sum(nums[:2])"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** The slice `nums[:2]` safely handles lists shorter than 2 (e.g., `[]` gives `[]`, `[1]` gives `[1]`). The `sum()` function on an empty list returns 0, and on a list with one element, it returns that element, perfectly matching the requirements."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `middle_way`\n",
    "\n",
    "**Question:** Given 2 int arrays, `a` and `b`, each length 3, return a new array length 2 containing their middle elements."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def middle_way(a, b):\n",
    "  return [a[1],b[1]]"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** We directly access the middle element (index 1) of both arrays and return them in a new list."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `make_ends`\n",
    "\n",
    "**Question:** Given an array of ints, return a new array length 2 containing the first and last elements from the original array. The original array will be length 1 or more."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def make_ends(nums):\n",
    "  return [nums[0],nums[-1]]"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** We access the first element (`nums[0]`) and the last element (`nums[-1]`) and place them into a new list."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `has23`\n",
    "\n",
    "**Question:** Given an int array length 2, return `True` if it contains a 2 or a 3."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def has23(nums):\n",
    "  return (2 in nums) or (3 in nums)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** We use the `in` operator to check if `2` is present in the list OR if `3` is present."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## List-2: More Complex List Logic\n",
    "\n",
    "This section includes problems requiring more nuanced logic or iteration over lists."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `count_evens`\n",
    "\n",
    "**Question:** Return the number of even ints in the given array. Note: the `%` \"mod\" operator computes the remainder, e.g. 5 % 2 is 1."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def count_evens(nums):\n",
    "  count = 0\n",
    "  for i in nums:\n",
    "    if i%2==0:\n",
    "      count += 1\n",
    "  \n",
    "  return count"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** This code iterates through each number in the input list `nums`. If a number is even (its remainder when divided by 2 is 0), a `count` variable is incremented. Finally, the total `count` of even numbers is returned."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `big_diff`\n",
    "\n",
    "**Question:** Given an array length 1 or more of ints, return the difference between the largest and smallest values in the array. Note: the built-in `min(v1, v2)` and `max(v1, v2)` functions return the smaller or larger of two values."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def big_diff(nums):\n",
    "  return max(nums)-min(nums) "
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** Python has built-in `max()` and `min()` functions that work directly on lists, returning the largest and smallest elements respectively. We simply subtract the smallest from the largest."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `centered_average`\n",
    "\n",
    "**Question:** Return the \"centered\" average of an array of ints, which we'll say is the mean average of the values, except ignoring the largest and smallest values in the array. If there are multiple copies of the smallest value, ignore just one copy, and likewise for the largest value. Use int division to produce the final average. You may assume that the array is length 3 or more."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def centered_average(nums):\n",
    "  return sum(nums[1:-1])/(len(nums)-2)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** This solution attempts to sum elements excluding the first and last (using `nums[1:-1]`) and then divides by the count of remaining elements. For this to work correctly when ignoring *only one* copy of the min/max, the list should first be sorted. Without sorting, `nums[1:-1]` might not exclude the actual min/max if they are not at the ends of the unsorted array."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `sum13`\n",
    "\n",
    "**Question:** Return the sum of the numbers in the array, returning 0 for an empty array. Except the number 13 is very unlucky, so it does not count and numbers that come immediately after a 13 also do not count."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def sum13(nums):\n",
    "  if len(nums)<1:\n",
    "    return 0\n",
    "  sum = 0\n",
    "  for i in range(len(nums)):\n",
    "    if nums[i] == 13:\n",
    "      continue\n",
    "    elif nums[i-1] == 13:\n",
    "      continue\n",
    "    \n",
    "    sum += nums[i]\n",
    "  return sum"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** This code iterates through the array. If an element is 13, it's skipped. It also attempts to skip an element if the *previous* element was 13. This `nums[i-1]` check will cause an error for the first element (`i=0`) as `nums[-1]` refers to the last element, not an element before the start. The variable name `sum` also shadows the built-in `sum()` function."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `sum67`\n",
    "\n",
    "**Question:** Return the sum of the numbers in the array, except ignore sections of numbers starting with a 6 and extending to the next 7 (every 6 will be followed by at least one 7). Return 0 for no numbers."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def sum67(nums):\n",
    "  flag = False\n",
    "  sum = 0\n",
    "  for n in nums:\n",
    "    if n==6:\n",
    "      flag = True\n",
    "    elif n==7 and flag:\n",
    "      flag = False\n",
    "    elif not flag:\n",
    "      sum += n\n",
    "  return sum"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** A boolean flag `in_ignore_section` (named `flag` in the code) is used to manage state. When a `6` is found, the flag is set to `True`. Numbers are only added to `total_sum` (named `sum` in the code) if `in_ignore_section` is `False`. When a `7` is found *and* the flag is `True`, the flag is reset to `False`, ending the ignored section."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `has22`\n",
    "\n",
    "**Question:** Given an array of ints, return `True` if the array contains a 2 next to a 2 somewhere."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def has22(nums):\n",
    "  for n in range(len(nums)-1):\n",
    "    if nums[n] == 2 and nums[n+1] == 2:\n",
    "      return True\n",
    "  return False"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** We loop through the array up to the second-to-last element (`len(nums) - 1`). In each iteration, we check if the current element and the next element are both 2."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## String-2: More String Challenges\n",
    "\n",
    "This section continues with intermediate string problems."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `double_char`\n",
    "\n",
    "**Question:** Given a string, return a string where for every char in the original, there are two chars."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def double_char(str):\n",
    "  new_string = \"\"\n",
    "  for i in str:\n",
    "    new_string += i*2\n",
    "  return new_string\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** We iterate through each character in the input string. For each character, we append it doubled (`char * 2`) to a `new_string`."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `count_hi`\n",
    "\n",
    "**Question:** Return the number of times that the string \"hi\" appears anywhere in the given string."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def count_hi(str):\n",
    "  return str.count(\"hi\")"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** Python's built-in `str.count()` method directly counts non-overlapping occurrences of a substring. This is the most efficient and Pythonic solution."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `cat_dog`\n",
    "\n",
    "**Question:** Return `True` if the string \"cat\" and \"dog\" appear the same number of times in the given string."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def cat_dog(str):\n",
    "  return str.count('cat') == str.count('dog')\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** We use the `str.count()` method for both \"cat\" and \"dog\" and then compare their counts directly."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `count_code`\n",
    "\n",
    "**Question:** Return the number of times that the string \"code\" appears anywhere in the given string, except we'll accept any letter for the 'd', so \"cope\" and \"cooe\" count."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def count_code(str):\n",
    "  count = 0\n",
    "  i=0\n",
    "  while(i<len(str)-3):\n",
    "    if str[i:i+2]=='co' and str[i+3] == 'e':\n",
    "      count += 1\n",
    "    i += 1\n",
    "  \n",
    "  return count"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** We iterate through the string with a `while` loop, checking 4-character windows. The condition `str_val[i:i+2] == 'co' and str_val[i+3] == 'e'` specifically looks for 'co' followed by any character (which is skipped by checking `i+3`) and then 'e'."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `end_other`\n",
    "\n",
    "**Question:** Given two strings, return `True` if either of the strings appears at the very end of the other string, ignoring upper/lower case differences (in other words, the computation should not be \"case sensitive\"). Note: `s.lower()` returns the lowercase version of a string."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def end_other(a, b):\n",
    "  a = a.lower()\n",
    "  b = b.lower()\n",
    "  return a.endswith(b) or b.endswith(a)\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** First, convert both strings to lowercase using `.lower()` to ensure case-insensitivity. Then, use the `str.endswith()` method to check if `a` ends with `b` OR if `b` ends with `a`."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `xyz_there`\n",
    "\n",
    "**Question:** Return `True` if the given string contains an appearance of \"xyz\" where the xyz is not directly preceeded by a period (.). So \"xxyz\" counts but \"x.xyz\" does not."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def xyz_there(str):\n",
    "  for i in range(len(str)-2):\n",
    "    if str[i:i+3] == \"xyz\" and str[i-1] != \".\":\n",
    "      return True\n",
    "  \n",
    "  return False"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** This code iterates through the string, looking for \"xyz\". For each \"xyz\" found, it checks if the character immediately preceding it (`str_val[i-1]`) is not a period. Note that `str_val[i-1]` will cause an `IndexError` if `i` is 0. A more robust solution would explicitly check `i == 0` or ensure the index is valid."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Logic-1: Basic Boolean Logic\n",
    "\n",
    "This section focuses on problems involving `if/else` and boolean operations."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `cigar_party`\n",
    "\n",
    "**Question:** When squirrels get together for a party, they like to have cigars. A squirrel party is successful when the number of cigars is between 40 and 60, inclusive. Unless it is the weekend, in which case there is no upper bound on the number of cigars. Return `True` if the party with the given values is successful, or `False` otherwise."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def cigar_party(cigars, is_weekend):\n",
    "  return True if (cigars>=40 and cigars <=60) or (is_weekend and cigars>40) else False\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** This solution uses a conditional expression. It returns `True` if the cigars are between 40 and 60 (inclusive) OR if it's the weekend AND cigars are greater than 40. Note that the problem states 'no upper bound' on the weekend, so `cigars > 40` should ideally be `cigars >= 40` for consistency with the lower bound."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `date_fashion`\n",
    "\n",
    "**Question:** You and your date are trying to get a table at a restaurant. The parameter \"you\" is the stylishness of your clothes, in the range 0..10, and \"date\" is the stylishness of your date's clothes. The result getting the table is encoded as an int value with 0=no, 1=maybe, 2=yes. If either of you is very stylish, 8 or more, then the result is 2 (yes). With the exception that if either of you has style of 2 or less, then the result is 0 (no). Otherwise the result is 1 (maybe)."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def date_fashion(you, date):\n",
    "  if (you >=8 or date >= 8) and not (you <3 or date <3):\n",
    "    return 2\n",
    "  elif you <=2 or date<=2:\n",
    "    return 0\n",
    "  else:\n",
    "    return 1"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** This solution uses an `if-elif-else` structure. It first checks if either person is very stylish (>=8) AND neither is very unstylish (<3) to return 2. Then, it checks if either is very unstylish to return 0. Otherwise, it defaults to 1. The order of checks is important to correctly apply the rules."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `squirrel_play`\n",
    "\n",
    "**Question:** The squirrels in Palo Alto spend most of the day playing. In particular, they play if the temperature is between 60 and 90 (inclusive). Unless it is summer, then the upper limit is 100 instead of 90. Given an int `temperature` and a boolean `is_summer`, return `True` if the squirrels play and `False` otherwise."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def squirrel_play(temp, is_summer):\n",
    "  return True if (temp >= 60 and temp<=90) or (is_summer and (temp >= 60 and temp<=100)) else False\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** This uses a conditional expression. It returns `True` if the temperature is within the 60-90 range (inclusive) OR if it's summer AND the temperature is within the 60-100 range (inclusive). The `True if ... else False` structure can be simplified to just the boolean expression itself."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `caught_speeding`\n",
    "\n",
    "**Question:** You are driving a little too fast, and a police officer stops you. Write code to compute the result, encoded as an int value: 0=no ticket, 1=small ticket, 2=big ticket. If speed is 60 or less, the result is 0. If speed is between 61 and 80 inclusive, the result is 1. If speed is 81 or more, the result is 2. Unless it is your birthday -- on that day, your speed can be 5 higher in all cases."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def caught_speeding(speed, is_birthday):\n",
    "  if (is_birthday and speed <= 65) or speed<=60:\n",
    "    return 0\n",
    "  elif (is_birthday and speed >65 and speed<=85)  or (speed >60 and speed<=80):\n",
    "    return 1\n",
    "  else:\n",
    "    return 2"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** This solution uses `if-elif-else` to determine the ticket level. It combines the birthday adjustment directly into the speed comparisons. For example, for no ticket, it checks if `speed` is <= 65 on birthday OR <= 60 otherwise. This pattern continues for small and big tickets."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `sorta_sum`\n",
    "\n",
    "**Question:** Given 2 ints, `a` and `b`, return their sum. However, sums in the range 10..19 inclusive, are forbidden, so in that case just return 20."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def sorta_sum(a, b):\n",
    "  return 20 if a+b >=10 and a+b <=19 else a+b"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** Calculate the sum first. Then, use a conditional expression to check if `current_sum` falls within the forbidden range (10 to 19 inclusive). If it does, return 20; otherwise, return the actual sum."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `alarm_clock`\n",
    "\n",
    "**Question:** Given a day of the week encoded as 0=Sun, 1=Mon, 2=Tue, ...6=Sat, and a boolean indicating if we are on vacation, return a string of the form \"7:00\" indicating when the alarm clock should ring. Weekdays, the alarm should be \"7:00\" and on the weekend it should be \"10:00\". Unless we are on vacation -- then on weekdays it should be \"10:00\" and weekends it should be \"off\"."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def alarm_clock(day, vacation):\n",
    "  if (day>0 and day<6) and not vacation:\n",
    "    return '7:00'\n",
    "  elif (day==0 or day==6) and vacation:\n",
    "    return 'off'\n",
    "  else:\n",
    "    return '10:00'"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** This solution uses an `if-elif-else` structure to cover the conditions. It first checks for weekdays not on vacation (7:00). Then, it checks for weekends on vacation ('off'). Any other case (weekdays on vacation or weekends not on vacation) defaults to '10:00'."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `love6`\n",
    "\n",
    "**Question:** The number 6 is a truly great number. Given two int values, `a` and `b`, return `True` if either one is 6. Or if their sum or difference is 6. Note: the function `abs(num)` computes the absolute value of a number."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def love6(a, b):\n",
    "  return True if (a==6 or b==6) or (abs(a-b)==6 or (a+b)==6) else False"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** This is a direct translation of the rules into a single boolean expression using `or`. It checks if `a` is 6, or `b` is 6, or their sum is 6, or their absolute difference is 6. The `True if ... else False` structure can be simplified to just the boolean expression itself."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `in1to10`\n",
    "\n",
    "**Question:** Given a number `n`, return `True` if `n` is in the range 1..10, inclusive. Unless `outside_mode` is `True`, in which case return `True` if the number is less or equal to 1, or greater or equal to 10."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def in1to10(n, outside_mode):\n",
    "  return True if(n>0 and n<11 and not outside_mode) or (outside_mode and (n<=1 or n>=10)) else False\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** This uses a conditional expression. It returns `True` if `n` is between 1 and 10 (exclusive of 0 and 11) AND `outside_mode` is `False`, OR if `outside_mode` is `True` AND `n` is less than or equal to 1 OR greater than or equal to 10. The `True if ... else False` structure can be simplified to just the boolean expression itself."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `near_ten`\n",
    "\n",
    "**Question:** Given a non-negative number \"num\", return `True` if `num` is within 2 of a multiple of 10. Note: (`a % b`) is the remainder of dividing `a` by `b`, so (7 % 5) is 2."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def near_ten(num):\n",
    "  return num % 10 <= 2 or num % 10 >= 8"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** We get the remainder when `num` is divided by 10. If this remainder is 0, 1, or 2, it means `num` is a multiple of 10, 1 more, or 2 more. If the remainder is 8 or 9, it means `num` is 2 less or 1 less than the *next* multiple of 10. Both sets of remainders satisfy the \"within 2\" condition."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Logic-2: Advanced Logic and Problem Solving\n",
    "\n",
    "These problems require a bit more thought and sometimes helper functions."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `make_bricks`\n",
    "\n",
    "**Question:** We want to make a row of bricks that is `goal` inches long. We have a number of small bricks (1 inch each) and big bricks (5 inches each). Return `True` if it is possible to make the `goal` by choosing from the given bricks. This is a little harder than it looks and can be done without any loops."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def make_bricks(small, big, goal):\n",
    "  using_big_bars = min(big,goal//5)\n",
    "  needed_small_bars = goal - using_big_bars*5\n",
    "  return needed_small_bars if small>= needed_small_bars else -1"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** This solution prioritizes using 5-inch big bars. It calculates the maximum number of big bars that can be used without exceeding the `goal` (`min(big, goal // 5)`). Then, it determines the `needed_small_bars` to cover the remaining length. If the available `small` bars are sufficient (`small >= needed_small_bars`), it returns the number of small bars needed; otherwise, it returns -1."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `lone_sum`\n",
    "\n",
    "**Question:** Given 3 int values, `a b c`, return their sum. However, if one of the values is the same as another of the values, it does not count towards the sum."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def lone_sum(a, b, c):\n",
    "  return (a if a != b and a != c else 0) + (b if b != a and b != c else 0) + (c if c != a and c != b else 0)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** For each number (`a`, `b`, `c`), a conditional expression is used. The number is added to the total sum only if it is not equal to either of the other two numbers. Otherwise, `0` is added, effectively excluding it from the sum."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `lucky_sum`\n",
    "\n",
    "**Question:** Given 3 int values, `a b c`, return their sum. However, if one of the values is 13 then it does not count towards the sum and values to its right do not count. So for example, if `b` is 13, then both `b` and `c` do not count."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def lucky_sum(a, b, c):\n",
    "  return (a if a != 13 else 0) + (b if b!=13 and a!=13 else 0) + (c if c!=13 and b!=13 and a != 13 else 0)\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** This solution uses nested conditional expressions to apply the \"13 and to its right\" rule. Each number is added only if it's not 13 AND the numbers to its left were also not 13. This correctly implements the short-circuiting behavior."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `no_teen_sum`\n",
    "\n",
    "**Question:** Given 3 int values, `a b c`, return their sum. However, if any of the values is a teen -- in the range 13..19 inclusive -- then that value counts as 0, except 15 and 16 do not count as a teens. Write a separate helper \"def fix_teen(n):\" that takes in an int value and returns that value fixed for the teen rule. In this way, you avoid repeating the teen code 3 times (i.e. \"decomposition\"). Define the helper below and at the same indent level as the main `no_teen_sum()`."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def fix_teens(n):\n",
    "  return True if (n>=13 and n<=19) and not (n == 15 or n==16) else False\n",
    "\n",
    "def no_teen_sum(a, b, c):\n",
    "  return (a if not fix_teens(a) else 0) + (b if not fix_teens(b) else 0) +(c if not fix_teens(c) else 0)\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:**\n",
    "* **`fix_teens(n)`:** This helper function attempts to identify \"bad teen\" numbers. It returns `True` if a number is in the 13-19 range AND is not 15 or 16. Otherwise, it returns `False`. The problem statement typically expects this helper to return the *fixed value* (0 or `n`), not a boolean.\n",
    "* **`no_teen_sum(a, b, c)`:** This function uses conditional expressions. If `fix_teens()` returns `True` (meaning it's a \"bad teen\"), it adds 0; otherwise, it adds the original number. This approach correctly uses the boolean output of `fix_teens` to determine what to add to the sum."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `round_sum`\n",
    "\n",
    "**Question:** For this problem, we'll round an int value up to the next multiple of 10 if its rightmost digit is 5 or more, so 15 rounds up to 20. Alternately, round down to the previous multiple of 10 if its rightmost digit is less than 5, so 12 rounds down to 10. Given 3 ints, `a b c`, return the sum of their rounded values. To avoid code repetition, write a separate helper \"def round10(num):\" and call it 3 times. Write the helper entirely below and at the same indent level as the main `round_sum()`."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def round10(num):\n",
    "  mod = num%10\n",
    "  if mod < 5:\n",
    "    return num-mod\n",
    "  else:\n",
    "    return num+(10-mod)\n",
    "  \ndef round_sum(a, b, c):\n",
    "  return round10(a)+round10(b)+round10(c)\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:**\n",
    "* **`round10(num)`:** This helper function calculates the `remainder` when `num` is divided by 10 (which is its last digit). If `remainder` is less than 5, it subtracts the `remainder` to round down. Otherwise, it adds `(10 - remainder)` to round up to the next multiple of 10.\n",
    "* **`round_sum(a, b, c)`:** This function simply calls `round10` for each of the three input numbers and sums their rounded results, effectively using the helper for decomposition."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `close_far`\n",
    "\n",
    "**Question:** Given three ints, `a b c`, return `True` if one of `b` or `c` is \"close\" (differing from `a` by at most 1), while the other is \"far\", differing from both other values by 2 or more. Note: `abs(num)` computes the absolute value of a number."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def close_far(a, b, c):\n",
    "  return True if (abs(a-b)<=1 and abs(a-c)>1 and abs(b-c)>1) or (abs(a-b)>1 and abs(a-c)<=1 and abs(b-c)>1) else False\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** This solution explicitly checks two scenarios using `or`.\n",
    "1.  `b` is close to `a` (`abs(a-b)<=1`), AND `c` is far from `a` (`abs(a-c)>1`), AND `c` is far from `b` (`abs(b-c)>1`).\n",
    "2.  `c` is close to `a` (`abs(a-c)<=1`), AND `b` is far from `a` (`abs(a-b)>1`), AND `b` is far from `c` (`abs(b-c)>1`).\n",
    "The `True if ... else False` structure can be simplified to just the boolean expression itself."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### `make_chocolate`\n",
    "\n",
    "**Question:** We want to make a package of `goal` kilos of chocolate. We have small bars (1 kilo each) and big bars (5 kilos each). Return the number of small bars to use, assuming we always use big bars before small bars. Return -1 if it can't be done."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**My Original Solution:**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "def make_chocolate(small, big, goal):\n",
    "  using_big_bars = min(big,goal//5)\n",
    "  needed_small_bars = goal - using_big_bars*5\n",
    "  return needed_small_bars if small>= needed_small_bars else -1"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Explanation:** This solution prioritizes using 5-inch big bars. It calculates the maximum number of big bars that can be used without exceeding the `goal` (`min(big, goal // 5)`). Then, it determines the `needed_small_bars` to cover the remaining length. If the available `small` bars are sufficient (`small >= needed_small_bars`), it returns the number of small bars needed; otherwise, it returns -1."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Conclusion\n",
    "\n",
    "This compilation represents my progress through various Python problems on CodingBat. I've found that breaking down problems into smaller, manageable parts, leveraging Python's built-in functions and understanding boolean logic are key to writing clean and effective code. CodingBat has been instrumental in solidifying my understanding of these concepts. I hope these solutions and explanations provide a clear insight for anyone on their Python learning journey!\n",
    "\n",
    "Happy coding!"
   ]
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3 (ipykernel)",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.12.0"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}
