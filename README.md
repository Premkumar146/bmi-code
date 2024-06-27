bmi code
def calculate_bmi():
    unit_system = input("Choose the unit system: \n1. Metric (kg, cm) \n2. Imperial (lbs, inches) \n3. Imperial (lbs, feet and inches) \nEnter 1 or 2 or 3: ")

    if unit_system == '1':
        weight = float(input("Enter the weight in kg: "))
        height = float(input("Enter the height in cm: "))
        bmi = weight / (height / 100) ** 2
    elif unit_system == '2':
        weight = float(input("Enter the weight in lbs: "))
        height = float(input("Enter the height in inches: "))
        bmi = (weight / (height ** 2)) * 703
    elif unit_system == '3':
        weight_lbs = float(input("Enter the weight in lbs: "))
        height_feet = float(input("Enter the height in feet: "))
        height_inches = float(input("Enter the remaining height in inches: "))
        height_total_inches = height_feet * 12 + height_inches
        bmi = (weight_lbs / (height_total_inches ** 2)) * 703
    else:
        print("Invalid choice. Please enter 1, 2, or 3.")
        return

    print("Your BMI is", bmi)

    if bmi <= 18.5:
        print("You are underweight")
    elif bmi <= 24.9:
        print("You are healthy")
    elif bmi <= 29.9:
        print("You are overweight")
    else:
        print("You are obese")

calculate_bmi()
