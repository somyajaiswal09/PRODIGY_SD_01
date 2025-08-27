
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



```

