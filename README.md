<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
</head>
<body>
  <h1 align="center">Inventory Tracker</h1>
  <br>
  <p align="center">
    <strong>By: Ryan Hatch</strong><br>
  </p>
<p align="center">
  <strong>Analyze and manage purchases for the Corner Grocer</strong>
</p>
<p align="center">
  <a href="#introduction">Introduction</a> •
  <a href="#design-and-functionality">Design and Functionality</a> •
  <a href="#usage">Usage</a> •
  <a href="#objective-oriented-programming">Objective Oriented Programming</a> •
    <a href="#journal">Journal</a> •
<!--  <a href="#screenshots">Screenshots</a> • -->
<!--  <a href="#contributing">Contributing</a> • -->
  <a href="#license">License</a>
</p>
<br>
<picture>
  <div style="text-align">
    <div align="center">
      <source media="(prefers-color-scheme: dark)" srcset="https://github.com/ryanshatch/Inventory-Tracker/blob/main/inventory%20tracker.jpg">
      <img alt=" " src="https://github.com/ryanshatch/Inventory-Tracker/blob/main/inventory%20tracker.jpg" style="width: 100%; height: 100%;">
    </div>
  </div>
</picture>

## Introduction

The Inventory Tracker is a software application developed for the Corner Grocer to track, manage, and analyze the inventory throughout the day. The program allows the store to update and track the frequency of item purchases, print item lists with their frequencies, and generate text-based histograms representing the purchase frequency of each item.

<br>
</p>

## Design and Functionality

The program is implemented using C++ and follows industry-standard best practices for code organization and readability. It consists of multiple files, including `Main.cpp`, `GroceryTracker.cpp`, `GroceryTrackerHeader.h`, `Inventory.txt`, and `Frequency.dat`. The main functionality is encapsulated in the `GroceryTracker` class, which handles the loading of records, searching for items, generating lists and histograms, as well as saving and updating data.

The program provides the following menu options:

1. **Search or update an item and return its frequency:** This option prompts the user whether they would like to search or update before prompting to input the slected item. The program will then prompt the user to update the frequency of the item by inputting the *amount* of the selected item to *add or subtract from the records.*
2. **Print list with item frequencies:** This option prints a list of all items along with their respective frequencies.
3. **Print item frequencies as a histogram:** This option generates a text-based histogram representation of the item frequencies.
4. **Exit:** This option will save all updates to a .dat file before allowing the user to exit the program.

The program then reads the input records from the file `Inventory.txt`. The file contains a list of items purchased throughout the day, with each item on a separate line. The records are loaded into a `std::map` data structure within the `GroceryTracker` class, where the item names serve as keys, and the frequencies are stored as values.
<br>
<br>

**The Inventory-Tracking program utilizes file I/O operations to load the records from the input file and save the accumulated data to the `Frequency.dat` file for backup purposes.**

<br>
</p>

## Usage
To use the Inventory Tracking Program, follow these steps:

1. `Clone the repository:`<br>
2. `Open the project in your preferred C++ development environment.`<br>
3. `Build and compile the project.`<br>
4. `Run the compiled executable file.`<br>
5. `Follow the on-screen prompts to navigate the program menu and perform the desired actions.`<br>

<br>
</p>

## Objective Oriented Programming

The Inventory Tracking Program includes robust input validation and error handling to ensure accurate and secure user interactions. The following validations have been implemented:

1. **Menu Choice Validation:** The program validates that the user's menu choice is within the valid range (1 to 4). If an invalid choice is entered, an error message is displayed, and the user is prompted for input again.

2. **Item Search Validation:** When searching for an item, the program validates that the user enters a non-empty item name. If an empty name is provided, an error message is displayed, and the user is prompted for input again.

3. **Input Data Type Validation:** The program validates that the user enters the correct data type when required. For example, if the program expects an integer input for the quantity to update, it verifies that the user enters a valid integer value. If an invalid value is provided, an error message is displayed, and the user is prompted for input again.

These input validation techniques enhance the robustness and user-friendliness of the program, preventing potential errors and ensuring a smooth user experience.

```By implementing input validation and error handling based on your specific requirements and preferences, you can provide a more user-friendly experience and reduce the likelihood of runtime errors. If you would like to explore additional validation techniques or error handling mechanisms within the item tracker, feel free to customize the program according to your needs.```

<!--## Screenshots
Include relevant screenshots here to showcase the program's functionality -->
<!-- ![Screenshot 1](screenshots/screenshot1.png) -->
<!-- ![Screenshot 2](screenshots/screenshot2.png) -->
<br>
</p>

## Journal

#### Summarize the project and what problem it was solving.

- The Grocery Tracker application was developed with the aim of assisting users in efficiently managing their grocery items and monitoring their purchase frequencies. It provides a wide array of valuable features, including the ability to load grocery records from a file, search for and update items, generate lists and histograms, and save data for future reference. The primary objective of this application is to tackle the common challenge of organizing and keeping track of grocery items, offering users a user-friendly tool to streamline their grocery management process.

#### What did you do particularly well?

- One particular strength of this project is the careful design and implementation of the GroceryTracker class. It serves as the core component of the application, neatly encapsulating the essential functionality. By using the std::map container to store and manage item frequencies, the code becomes more modular and flexible, making it easier to maintain and expand upon.

#### Where could you enhance your code? How would these improvements make your code more efficient, secure, and so on?

- To further improve the code, there are several areas worth considering.
  - Optimizing the data structures and algorithms utilized. Exploring alternative containers or improving search operations can have a substantial impact on the code's efficiency and performance.
  - Another area of improvement involves integrating logging functionalities and error reporting features. This addition would facilitate easier debugging and troubleshooting, making it a smooth process to identify and address potential issues. By enhancing the code's maintainability, developers can more efficiently diagnose and resolve problems, ultimately leading to a more robust and stable application.

#### Which pieces of the code did you find most challenging to write, and how did you overcome this? What tools or resources are you adding to your support network?

- One of the most demanding aspects of the code implementation was the creation of a histogram to visualize item frequencies within the printHistogram function. Tackling this challenge required meticulous iteration over the items and their frequencies, as well as determining the optimal scale for the histogram and formatting the output to produce a visually meaningful representation. To overcome this hurdle, I found great value in consulting online resources, referring to C++ documentation, and exploring various approaches. Additionally, YouTube tutorials provided helpful insights and practical guidance throughout the process.

#### What skills from this project will be particularly transferable to other projects or course work?

- Engaging in this project has equipped me with a multitude of valuable skills that can be readily applied to other projects and coursework. I have gained a solid understanding of object-oriented design principles, enabling me to create well-structured and modular code. Working with standard library containers has provided me with practical experience in effectively managing data structures. Additionally, implementing file input/output operations has given me insights into data persistence and management. The ability to validate user input has become second nature, ensuring robust and error-free interactions. Through this project, I have also honed my skills in creating intuitive user interfaces, enhancing the overall user experience. These acquired skills will undoubtedly prove invaluable in future endeavors, be it application development, software engineering, or further programming coursework.

#### How did you make this program maintainable, readable, and adaptable?

- To guarantee the code's long-term maintainability, readability, and adaptability, I implemented a set of best practices. With OOP in mind, these practices encompassed decomposing functionalities into modular functions and classes, employing clear and descriptive names for variables and functions, providing comments to clarify intricate sections, adhering to established coding conventions and style guidelines, and striving for clean and concise code. Furthermore, the utilization of the documentation of the project, dependencies, and setup instructions greatly contributed to the code's overall maintainability and adaptability.

<br>
</p>

## License

This software is the property of the copyright holder and is protected by copyright laws. All rights are reserved.

The copyright holder grants no implied or express license for the use, copying, modification, distribution, or reproduction of this software, in whole or in part, without the prior written permission of the copyright holder.

Any unauthorized use, copying, modification, distribution, or reproduction of this software, in whole or in part, is strictly prohibited and constitutes a violation of copyright law. Such unauthorized use may result in civil and/or criminal penalties, including but not limited to legal action and monetary damages.

To obtain permission for any use, copying, modification, distribution, or reproduction of this software, please contact the copyright holder at the following address:

```ryanshatch@gmail.com```
<br>
<br>
<br>
```By using this software, you acknowledge that you have read and understood the terms of this license and agree to comply with all applicable copyright laws. Failure to abide by the terms of this license may subject you to legal consequences.```
