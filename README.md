# bmi-code
def calculate_bmi():
    unit_system = input("Choose the unit system: \n1. Metric (cm, kg) \n2. Imperial (inches, lbs) \nEnter 1 or 2: ")

    if unit_system == '1':
        height = float(input("Enter the height in cm: "))
        weight = float(input("Enter the weight in kg: "))
        bmi = weight / (height / 100) ** 2
    elif unit_system == '2':
        height = float(input("Enter the height in inches: "))
        weight = float(input("Enter the weight in lbs: "))
        bmi = (weight / (height ** 2)) * 703
    else:
        print("Invalid choice. Please enter 1 or 2.")
        return

    print("Your BMI is", bmi)

    if bmi <= 18.5:
        print("You are underweight")
    else:
        if bmi <= 24.9:
            print("You are healthy")
        else:
            if bmi <= 29.9:
                print("You are overweight")
            else:
                print("You are obese")

calculate_bmi()
