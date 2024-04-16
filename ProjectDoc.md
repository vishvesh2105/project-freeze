**Program Documentation: Crime Data Analysis**

---

**Overview:**
This program is designed to analyze crime data within a specified radius of a given location. It loads crime data from a text file, calculates distances between crime locations and a target location using the Haversine formula, and identifies crimes within the specified radius. The user can input a location and a radius to retrieve crime data for that area.

**Parts:**

1. **Data Loading and Processing:**
   - The program defines a structure `CrimeData` to store information about each crime, including location, type, latitude, and longitude.
   - The function `loadCrimeData` reads crime data from a text file and populates an array of `CrimeData` objects.

2. **Geospatial Calculations:**
   - The function `calculateDistance` implements the Haversine formula to calculate the distance between two sets of coordinates.
   - The function `getCrimesInRadius` uses the calculated distance to find crimes within a specified radius of a given coordinate.

3. **User Interaction and Input:**
   - The `main` function manages user interaction and input.
   - It prompts the user to enter a location and a radius, maps the location to its corresponding latitude and longitude, and calls the relevant functions to analyze crime data.

4. **Output and Memory Management:**
   - The function `displayCrimeData` outputs crime data to the console.
   - Memory allocated dynamically during program execution is deallocated at the end of the program to prevent memory leaks.

**Usage:**
1. Compile the program using a C++ compiler.
2. Ensure that the crime data is stored in a text file named "crime_data.txt" in the specified format (location, type, latitude, longitude).
3. Run the compiled executable.
4. Enter a location and a radius when prompted.
5. View the list of crimes within the specified radius.

**Dependencies:**
- The program requires the `<iostream>`, `<fstream>`, `<sstream>`, `<string>`, and `<cmath>` standard C++ libraries for input/output operations, file handling, string manipulation, and mathematical calculations.

**Notes:**
- Ensure that the crime data file is accessible and correctly formatted for proper program execution.
- The Haversine formula used for distance calculation assumes a spherical Earth model and may not be entirely accurate for all locations.
- The program currently supports specific locations (Kitchener, Waterloo, Chicopee, Guelph, Cambridge) with hardcoded latitude and longitude values. Additional locations can be added as needed.


