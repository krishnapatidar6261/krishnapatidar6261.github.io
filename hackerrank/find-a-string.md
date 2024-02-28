## Problem 
<p> In this challenge, the user enters a string and a substring. You have to print the number of times that the substring occurs in the given string. String traversal will take place from left to right, not from right to left. </p>

NOTE: String letters are case-sensitive. <br>

Input Format <br>

<p> 
    The first line of input contains the original string. The next line contains the substring.
</p>

### Constraints


Each character in the string is an ascii character.

### Output Format<br>

Output the integer number indicating the total number of occurrences of the substring in the original string.

### Sample Input<br>

ABCDCDC<br>
CDC<br>
Sample Output<br>

2

<br><br>

### Concept

<p> Some string processing examples, such as these, might be useful. <br>
    There are a couple of new concepts:<br>
    In Python, the length of a string is found by the function len(s), where  is the string. <br>
    To traverse through the length of a string, use a for loop: <br>
</p>

for i in range(0, len(s)): <br>
    print (s[i]) <br>
A range function is used to loop over some length:<br>

range (0, 5)<br>
Here, the range loops over  to .  is excluded.<br>

### Language
 <python>
 <https://www.hackerrank.com/challenges/find-a-string/problem?isFullScreen=true> <br>
 <https://www.hackerrank.com/profile/krishnapatidar62>

## Solutions



### Solution of Given problem

 def count_substring(string, sub_string):
    
    sl=len(sub_string)
    count=0
    for i in range(len(string)):
        
        if sub_string == string[i:sl]:

            count+=1
            
            sl+=1
        
        else:
            sl+=1
   
    
    return count
 if __name__ == '__main__':
    string = input().strip()
    sub_string = input().strip()
    
    count = count_substring(string, sub_string)
    print(count)
