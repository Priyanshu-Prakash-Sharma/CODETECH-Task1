**Name**: Priyanshu Prakash Sharma                 
**Company**: CODTECH IT SOLUTIONS                             
**ID**: CT6WDS1818                               
**Domain**: Android Development                              
**Duration**: August to October 2024                           

## BMI Calculator App - Overview

### Project Description
The **BMI Calculator App** is an Android application developed using **Kotlin** and **Jetpack Compose**. The app allows users to calculate their **Body Mass Index (BMI)** based on their weight and height, using either the **metric** or **imperial** measurement system. The app is designed to be simple, intuitive, and visually appealing, incorporating modern Android development practices like declarative UI with Jetpack Compose.

### Features
1. **Splash Screen**:
   - The app features a splash screen with an animated delay of 3 seconds. During this time, an icon and the app name are displayed. After the delay, the main functionality of the app is revealed.
   
2. **Unit Selection**:
   - Users can choose between **Metric** or **Imperial** units for their input:
     - **Metric**: Weight in kilograms (kg) and height in centimeters (cm).
     - **Imperial**: Weight in pounds (lbs) and height in feet and inches.
   
3. **BMI Calculation**:
   - The app calculates BMI based on user input:
     - For **Metric units**, BMI is calculated as `weight (kg) / (height (m) * height (m))`.
     - For **Imperial units**, the weight is first converted from pounds to kilograms and the height from feet and inches to centimeters before calculating BMI using the same formula.
   
4. **Obesity Level Display**:
   - After calculating BMI, the app displays the corresponding **obesity level**, which categorizes BMI as:
     - Underweight
     - Normal weight
     - Overweight
     - Obese (Class I, II, III)
   
5. **Responsive Layout**:
   - The app layout is fully responsive, adjusting smoothly across different screen sizes and orientations. The UI is created using **Jetpack Compose**, making it declarative and reactive to state changes.

### Code Overview

1. **MainActivity**:
   - Handles the main lifecycle of the app, including the initialization of the splash screen and the main app interface.
   - Uses **`remember`** and **`LaunchedEffect`** for managing state and delaying transitions from splash screen to the main content.

2. **SplashScreen**:
   - A composable function displaying the app's icon and name. It fills the entire screen using a **Box** layout, centered both horizontally and vertically.

3. **BmiCalculatorApp**:
   - This is the core composable that manages user input and BMI calculation. It provides UI elements for:
     - **Unit selection** (Metric or Imperial)
     - **Weight input** and **Height input** fields
     - **BMI calculation button**
     - Displaying **BMI result** and **obesity level**

4. **UnitSelection**:
   - A composable that allows the user to toggle between Metric and Imperial units using radio buttons.

5. **BMI Calculation Logic**:
   - **`calculateBMI()`**: This function computes the BMI based on the user's input and the selected measurement system (Metric or Imperial).
   - **`getObesityLevel()`**: This function takes the BMI result and returns a string indicating the user’s obesity category (Underweight, Normal weight, etc.).

### Future Enhancements
- **Error Handling**: Add more robust input validation, ensuring users provide valid numeric input before calculating BMI.
- **User Preferences**: Store the user’s last selected unit (Metric/Imperial) and input values using SharedPreferences or Jetpack DataStore.
- **UI Enhancements**: Improve visual appeal by incorporating more advanced animations or design components from Material 3.

### Tools and Technologies
- **Kotlin**: The primary programming language used to build the app.
- **Jetpack Compose**: A modern Android UI toolkit used to create the UI in a declarative way.
- **Material 3**: The app uses Material Design components to create a visually appealing and consistent UI.

### How to Run the Project
1. Clone the repository from GitHub.
2. Open the project in **Android Studio**.
3. Sync Gradle files and install any required dependencies.
4. Run the app on an emulator or a physical device.
