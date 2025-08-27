
### Algorithm 

1. **Initialize Program**:

   * Display a prompt to the user to select the scale of the input temperature: Celsius, Fahrenheit, or Kelvin.
   * Ask the user to input the temperature value in the chosen scale.

2. **Conversion Logic**:

   * Based on the input scale, apply the corresponding conversion formulas to generate the temperature in the other two scales.

     * **Celsius to Fahrenheit and Kelvin**:

       * **Fahrenheit**: `F = (C * 9/5) + 32`
       * **Kelvin**: `K = C + 273.15`
     * **Fahrenheit to Celsius and Kelvin**:

       * **Celsius**: `C = (F - 32) * 5/9`
       * **Kelvin**: `K = (F - 32) * 5/9 + 273.15`
     * **Kelvin to Celsius and Fahrenheit**:

       * **Celsius**: `C = K - 273.15`
       * **Fahrenheit**: `F = (K - 273.15) * 9/5 + 32`

3. **Display Results**:

   * After performing the necessary conversions, display the converted temperatures in the other two scales.

4. **Repeat or Exit**:

   * Ask the user if they want to perform another conversion.
   * Exit if the user chooses to stop.

---

### Skills Used:

1. **Programming Language**:

   * C for implementing the conversion logic.

2. **Mathematical Operations**:

   * Arithmetic operations for temperature conversions between the scales.

3. **User Input**:

   * `scanf()` for accepting the temperature value and scale choice from the user.

4. **Conditionals**:

   * `if-else` or `switch-case` statements to handle the input scale and perform the corresponding conversions.

5. **Output**:

   * `printf()` to display the converted temperatures in the other two scales.

6. **Control Flow**:

   * Loops (e.g., `while` or `do-while`) to allow repeated conversions.

7. **Data Types**:

   * Use of floating-point data types (`float` or `double`) for precision in temperature values and conversions.

### Sample Code:

```c
#include <stdio.h>

void convertTemperature(float temp, int scale) {
    float celsius, fahrenheit, kelvin;
    
    if (scale == 1) {  // Celsius
        celsius = temp;
        fahrenheit = (celsius * 9/5) + 32;
        kelvin = celsius + 273.15;
    }
    else if (scale == 2) {  // Fahrenheit
        fahrenheit = temp;
        celsius = (fahrenheit - 32) * 5/9;
        kelvin = (fahrenheit - 32) * 5/9 + 273.15;
    }
    else if (scale == 3) {  // Kelvin
        kelvin = temp;
        celsius = kelvin - 273.15;
        fahrenheit = (kelvin - 273.15) * 9/5 + 32;
    }
    
    // Display the conversions
    printf("Converted Temperatures:\n");
    printf("Celsius: %.2f\n", celsius);
    printf("Fahrenheit: %.2f\n", fahrenheit);
    printf("Kelvin: %.2f\n", kelvin);
}

int main() {
    int scale;
    float temperature;

    printf("Temperature Converter\n");
    printf("Select input scale (1: Celsius, 2: Fahrenheit, 3: Kelvin): ");
    scanf("%d", &scale);

    printf("Enter the temperature value: ");
    scanf("%f", &temperature);

    // Validate scale input
    if (scale < 1 || scale > 3) {
        printf("Invalid scale selection! Please restart the program.\n");
        return 1;
    }

    // Perform conversion and display results
    convertTemperature(temperature, scale);

    return 0;
}
```

### Explanation of the Code:

1. **User Input**:

   * The user selects the scale (Celsius, Fahrenheit, or Kelvin) and inputs the temperature value.

2. **Conversion Logic**:

   * The `convertTemperature()` function handles the conversion based on the selected scale.
   * If Celsius is selected, it converts the input to Fahrenheit and Kelvin.
   * If Fahrenheit is selected, it converts the input to Celsius and Kelvin.
   * If Kelvin is selected, it converts the input to Celsius and Fahrenheit.

3. **Display Results**:

   * The program prints the converted temperatures in all the scales.

4. **Input Validation**:

   * The program checks that the scale is valid (1, 2, or 3).

---


