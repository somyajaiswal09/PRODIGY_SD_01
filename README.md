
def celsius_to_fahrenheit(celsius):
    return (celsius * 9/5) + 32

def celsius_to_kelvin(celsius):
    return celsius + 273.15

def fahrenheit_to_celsius(fahrenheit):
    return (fahrenheit - 32) * 5/9

def fahrenheit_to_kelvin(fahrenheit):
    return (fahrenheit - 32) * 5/9 + 273.15

def kelvin_to_celsius(kelvin):
    return kelvin - 273.15

def kelvin_to_fahrenheit(kelvin):
    return (kelvin - 273.15) * 9/5 + 32

def convert_temperature(value, unit):
    unit = unit.lower()
    
    if unit == "celsius" or unit == "c":
        fahrenheit = celsius_to_fahrenheit(value)
        kelvin = celsius_to_kelvin(value)
        print(f"\n{value:.2f} °C is:")
        print(f"{fahrenheit:.2f} °F")
        print(f"{kelvin:.2f} K")

    elif unit == "fahrenheit" or unit == "f":
        celsius = fahrenheit_to_celsius(value)
        kelvin = fahrenheit_to_kelvin(value)
        print(f"\n{value:.2f} °F is:")
        print(f"{celsius:.2f} °C")
        print(f"{kelvin:.2f} K")

    elif unit == "kelvin" or unit == "k":
        celsius = kelvin_to_celsius(value)
        fahrenheit = kelvin_to_fahrenheit(value)
        print(f"\n{value:.2f} K is:")
        print(f"{celsius:.2f} °C")
        print(f"{fahrenheit:.2f} °F")

    else:
        print("\nInvalid unit. Please use Celsius (C), Fahrenheit (F), or Kelvin (K).")

def main():
    try:
        value = float(input("Enter the temperature value: "))
        unit = input("Enter the unit of measurement (Celsius, Fahrenheit, or Kelvin): ")
        convert_temperature(value, unit)
    except ValueError:
        print("\nInvalid input. Please enter a numeric temperature value.")

if __name__ == "__main__":
    main()
