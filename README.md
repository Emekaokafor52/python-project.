# python-project.
def calculate_life_expectancy(age, is_smoker, has_high_blood_pressure, is_high_fat_diet):
    life_expectancy = 80  # Default life expectancy
    if age <= 30:
        life_expectancy -= 5
    elif age >= 50:
        life_expectancy -= 10

    if is_smoker:
        life_expectancy -= 10

    if has_high_blood_pressure:
        life_expectancy -= 5

    if is_high_fat_diet:
        life_expectancy -= 5

    return life_expectancy

while True:
    print("Life Expectancy Calculator")
    print("1) A 33-year-old woman, non-smoker with normal blood pressure who eats a high fat diet.")
    print("2) A 19-year-old man, non-smoker with high blood pressure who eats a high fat diet.")
    print("3) A 50-year-old woman, non-smoker with high blood pressure who eats a high fat diet.")
    print("4) A 27-year-old man, smoker with high blood pressure who eats a low fat diet.")
    print("5) A 43-year-old woman, smoker with high blood pressure who eats a high fat diet.")
    print("6) A 17-year-old woman, non-smoker with normal blood pressure who eats a high fat diet.")
    print("7) Exit")
    
    choice = input("Select an option (1-7): ")

    if choice == '7':
        break

    if choice in ['1', '2', '3', '4', '5', '6']:
        age = int(choice[0])  # Extract the age from the choice
        is_smoker = 'smoker' in choice
        has_high_blood_pressure = 'high blood pressure' in choice
        is_high_fat_diet = 'high fat diet' in choice

        life_expectancy = calculate_life_expectancy(age, is_smoker, has_high_blood_pressure, is_high_fat_diet)

        print(f"Life expectancy: {life_expectancy} years")
    else:
        print("Invalid choice. Please select a valid option (1-7).")

print("Goodbye!")
