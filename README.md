# P2-BSIT-S8
#Defines a reusable function that accepting three parameters. 
#Adding the three activities and divides it. 
def calculate_average(a1, a2, a3):
    return (a1 + a2 + a3) / 3

#Defines a function that takes an input. 
#Evaluates the average standard performance of the students. 
def determine_status(avg):
    if avg >= 90:
        return "Excellent"
    elif avg >= 80:
        return "Very Good"
    elif avg >= 75:
        return "Passed"
    else:
        return "Failed"

print("------------------------------------")

print("=== STUDENT ACTIVITY SCORE SYSTEM ===")
#Prompting the user to enter the number of students that needs to be processed. 
num_students = int(input("How many students? "))

for i in range(1, num_students + 1):
    print()
    print(f"Student {i}")
    name = input("Enter name: ")
    act1 = float(input("Activity 1: "))
    act2 = float(input("Activity 2: "))
    act3 = float(input("Activity 3: "))
    
    avg = calculate_average(act1, act2, act3)
    status = determine_status(avg)
    print()
    print(f"Average: {avg:.2f}")
    print(f"Status: {status}")
print("------------------------------------")
