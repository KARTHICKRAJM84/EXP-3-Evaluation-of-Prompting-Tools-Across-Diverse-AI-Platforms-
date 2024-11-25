# EXP-3-Evaluation-of-Prompting-Tools-Across-Diverse-AI-Platforms-
##  NAME:KARTHICK RAJ M
## REG NO:212221040073
# Aim:
 To compare the performance, user experience, and response quality of different AI 
platforms (ChatGPT, Claude, Bard, Cohere Command, and Meta) within a specific use case, 
such as summarizing text or answering technical questions.
# Instructions:
1. Define the Use Case:
o Select a specific task for evaluation across platforms (e.g., summarizing a 
document, answering a technical question, or generating a creative story / Code).
o Ensure the use case is applicable to all platforms and will allow for comparison 
across response quality, accuracy, and depth.
2. Create a Set of Prompts:
o Prepare a uniform set of prompts that align with the chosen use case.
o Each prompt should be clear and precise, ensuring that all platforms are evaluated 
using the same input.
o Consider multiple prompts to capture the versatility of each platform in handling 
different aspects of the use case.
3. Run the Experiment on Each AI Platform:
o Input the prompts into each AI tool (ChatGPT, Claude, Bard, Cohere Command, and 
Meta) and gather the responses.
o Ensure the same conditions are applied for each platform, such as input format, 
time to respond, and prompt delivery.
o Record response times, ease of interaction with the platform, and any technical 
issues encountered.
4. Evaluate Response Quality:
o Assess each platform’s responses using the following criteria: 
Accuracy,Clarity,Depth,Relevance
5. Compare Performance:
o Compare the collected data to identify differences in performance across 
platforms.
o Identify any platform-specific advantages, such as faster response times, more 
accurate answers, or more intuitive interfaces.

# Question:
Implement the following functions.a def MoveHyphen(s) The function accepts a string “str” of 
length ‘n’, that contains alphabets and hyphens (-). Implement the function to move all hyphens(-) 
in the string to the front of the given string. 
NOTE:- Return null if str is null. 
Example :- Input: str.Move-Hyphens-to-Front 
Output: —MoveHyphenstoFront 
Sample Input Str: String-Compare
Sample Output- -StringCompare 
Sample Input Str: Welcome-to-the-New-String 
Sample Output- ----WelcometotheNewString
Result:
Chatgpt:
def MoveHyphen(s):
 # Check if the input is null or empty
 if s is None:
 return None
 
 # Separate the hyphens and the rest of the characters
 hyphens = ''.join([char for char in s if char == '-'])
 others = ''.join([char for char in s if char != '-'])
 
 # Concatenate the hyphens in front of the other characters
 return hyphens + others
# Example usage:
print(MoveHyphen("Move-Hyphens-to-Front")) # Output: "---MoveHyphenstoFront"
print(MoveHyphen("String-Compare")) # Output: "-StringCompare"
print(MoveHyphen("Welcome-to-the-New-String")) # Output: "----WelcometotheNewString"

blackbox:
def MoveHyphen(s):
 # Step 1: Check if the input string is None
 if s is None:
 return None
 
 # Step 2: Initialize counters for hyphens and a list for other characters
 hyphen_count = 0
 other_chars = []
 
 # Step 3: Iterate through each character in the string
 for char in s:
 if char == '-':
 hyphen_count += 1 # Count the hyphens
 else:
 other_chars.append(char) # Collect non-hyphen characters
 
 # Step 4: Create the result string with hyphens at the front
 result = '-' * hyphen_count + ''.join(other_chars)
 
 return result
# Example usage
print(MoveHyphen("Move-Hyphens-to-Front")) # Output: '----MoveHyphenstoFront'
print(MoveHyphen("String-Compare")) # Output: '-StringCompare'
print(MoveHyphen("Welcome-to-the-New-String")) # Output: '----WelcometotheNewString'

claude:
def MoveHyphen(s):
 # Check if string is None
 if s is None:
 return None
 # Count number of hyphens
 hyphen_count = s.count('-')
 # Remove all hyphens and create new string
 str_without_hyphen = s.replace('-', '')
 # Create final string with hyphens at front
 result = '-' * hyphen_count + str_without_hyphen 
 return result
# Test cases
def test_MoveHyphen():
 print("Test Case 1:")
 print("Input: String-Compare")
 print("Output:", MoveHyphen("String-Compare")) 
 print("\nTest Case 2:")
 print("Input: Move-Hyphens-to-Front")
 print("Output:", MoveHyphen("Move-Hyphens-to-Front"))
 print("\nTest Case 3:")
 print("Input: Welcome-to-the-New-String")
 print("Output:", MoveHyphen("Welcome-to-the-New-String"))
 print("\nTest Case 4:")
 print("Input: None")
 print("Output:", MoveHyphen(None))
# Run test cases
test_MoveHyphen()

# SUMMARY:
1. ChatGPT:
o Strengths: Provides clear explanations and is good for general coding assistance, but 
may not always deliver the most accurate or optimized code on the first attempt.
o Your experience: Likely found it helpful for understanding concepts and getting stepby-step guidance but needed adjustments for the code to work perfectly.
2. Claude:
o Strengths: Similar to ChatGPT in its conversational approach and providing Python 
code, though possibly less accurate for complex or niche tasks.
o Your experience: Probably found it useful for discussions but not as strong in precise 
code accuracy, requiring further refinement or testing.
3. Blackbox:
o Strengths: In my experience, Blackbox performed best in terms of code accuracy for 
Python. It likely provided more reliable solutions without needing many tweaks.
o Your experience: Blackbox stood out as the most accurate tool, meeting your 
expectations for correct, functional Python code more consistently.
In summary, from your perspective, Blackbox excelled in providing accurate Python code, while 
ChatGPT and Claude were better suited for understanding and discussing coding tasks but needed 
more fine-tuning in terms of accuracy.
