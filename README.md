# Python-BMI-Calculator
Body Mass Index calculator with Python
### Step-by-Step Explanation of the BMI Calculator Code

This Python program calculates the **Body Mass Index (BMI)** based on user input and classifies the BMI into different weight categories.

---

### **Step 1: Prompting the User for Input**
The program asks the user to enter their **name, weight (in pounds), and height (in inches)** using the `input()` function.

```python
Name = input('Enter your name:')
Weight = int(input('Enter your weight in pounds:'))
Height = int(input('Enter your height in inches:'))
```
- `input()` captures user input as a string.
- `int()` converts weight and height into integers for numerical calculations.

---

### **Step 2: BMI Calculation**
The **BMI formula** in pounds and inches is applied:

\[
BMI = \frac{\text{Weight (in pounds)} \times 703}{\text{Height (in inches)}^2}
\]

```python
BMI = (Weight * 703) / (Height * Height)
```
- The program multiplies the weight by `703` and divides it by the square of the height.

---

### **Step 3: Displaying the BMI Value**
The program prints the calculated BMI:

```python
print("Your BMI is:", (BMI))
```
- This displays the user's BMI value.

---

### **Step 4: BMI Classification & Feedback**
The program checks the **BMI category** using `if-elif` conditions and gives appropriate health advice.

```python
if BMI>0:
    if (BMI < 18.5):
        print(Name + ', you are underweight. You need to diet properly.')
    elif (BMI <= 24.9):
        print(Name + ", you are normal weight. You're in shape!")
    elif (BMI <= 29.9):
        print(Name + ', you are overweight. You need to workout more often.')
    elif (BMI <= 34.9):
        print(Name + ', you are obese. Cut down on your food intake and workout very often.')
    elif (BMI <= 39.9):
        print(Name + ', you are severely obese. Stop eating junk food, cut down on diet, and workout daily.')
    elif (BMI >= 40):
        print(Name + ', you are morbidly obese. See a doctor urgently for medical advice!')
```

- **Underweight:** BMI < 18.5  
- **Normal weight:** BMI between 18.5 and 24.9  
- **Overweight:** BMI between 25 and 29.9  
- **Obese:** BMI between 30 and 34.9  
- **Severely Obese:** BMI between 35 and 39.9  
- **Morbidly Obese:** BMI ≥ 40  

Each category gives a personalized message based on the user's name.

---

### **Step 5: Handling Invalid Input**
If BMI is not positive (e.g., user enters invalid data), an error message is displayed:

```python
else:
    print('Enter valid input')
```
- This ensures that BMI calculations make sense and prompts the user to enter correct values.

---

### **Final Output Example**
#### **User Input:**
```
Enter your name: Alex
Enter your weight in pounds: 180
Enter your height in inches: 70
```
#### **Output:**
```
Your BMI is: 25.84
Alex, you are overweight. You need to workout more often.
```

---

### **Improvements**
1. **Input Validation:** Ensure that weight and height are positive numbers.
2. **Float Inputs:** Allow decimal values for more accurate BMI.
3. **Formatted Output:** Display BMI with two decimal places for clarity.

Would you like a refined version of this code with improvements? 
