
# BMI Calculator Project

def calculate_bmi(weight, height):
    """
    Calculate the Body Mass Index (BMI).
    
    Parameters:
    weight (float): Weight in kilograms.
    height (float): Height in meters.
    
    Returns:
    float: The BMI value.
    """
    return weight / (height ** 2)

def bmi_category(bmi):
    """
    Determine the BMI category.
    
    Parameters:
    bmi (float): The BMI value.
    
    Returns:
    str: The category based on the BMI value.
    """
    if bmi < 18.5:
        return "Underweight"
    elif 18.5 <= bmi < 24.9:
        return "Normal weight"
    elif 25 <= bmi < 29.9:
        return "Overweight"
    else:
        return "Obesity"

def main():
    print("Welcome to the BMI Calculator!")
    
        # Get user input for weight and height
        weight = float(input("Enter your weight in kilograms: "))
        height = float(input("Enter your height in meters: "))
        
        # Check for valid input
        if weight <= 0 or height <= 0:
            print("Please enter positive values for weight and height.")
            return
        
        # Calculate BMI
        bmi = calculate_bmi(weight, height)
        
        # Get the BMI category
        category = bmi_category(bmi)
        
        # Display the results
        print(f"\nYour BMI is: {bmi:.2f}")
        print(f"You are categorized as: {category}")
    
    except ValueError:
        print("Invalid input. Please enter numerical values for weight and height.")

if __name__ == "__main__":
    main().


