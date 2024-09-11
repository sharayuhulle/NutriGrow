# NutriGrow
Introductory project

# Introduction

The "NutriGrow" application is a Java-based tool designed to assist in assessing and improving child nutrition. Utilizing Apache POI for data processing and the Swing framework for a user-friendly interface, NutriGrow enables users to input a child's height and weight to determine their nutritional status from an Excel spreadsheet. The application not only identifies malnutrition levels with precise tolerance but also offers tailored diet recommendations for various age groups. 

# Technologies Used

- Java: The core programming language to build the application.
- Apache POI: Used to read and process Excel files, extracting data like height and weight for malnutrition detection.
- Swing: Java's GUI toolkit used to create the graphical interface, allowing users to input height and weight values and display results.
- JOptionPane: A part of Swing, used to display dialog boxes for user interaction, including search results and diet plans.

# Procedure

1. User Input through GUI:
   - The user enters the child's height and weight using the graphical interface built with Swing.
   - The inputs are captured via JTextFields and handled by an ActionListener tied to the "Search" button.
2. Excel Data Reading (Apache POI):
   - The application reads the Excel file containing data on height, weight, and malnutrition levels.
   - Using Apache POI, it opens the file, iterates through rows and columns, and looks for the closest matching height.
   - A double comparison is performed using a small epsilon value to find a matching height in the dataset.
3. Malnutrition Level Detection:
   - Once the matching height is found, the application checks the corresponding weight ranges.
   - If the weight falls within a predefined range, the malnutrition level (severe, moderate, mild, or normal) is identified.
4. Diet Plan and Malnutrition Information:
   - Based on the detected malnutrition level, the user is provided with a result message.
   - For cases of malnutrition (moderate or mild), the application prompts the user to input the child’s age in months.
   - A tailored diet plan is generated based on both the malnutrition level and the child’s age, providing dietary recommendations.
5. Display of Results:
   - Results, including the malnutrition level and corresponding diet plan, are displayed in pop-up dialog boxes.
   - For severe malnutrition, the user is advised to consult a pediatrician.
