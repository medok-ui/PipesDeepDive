# Angular Pipes Deep Dive

A learning project from [Maximilian Schwarzmüller's](https://www.udemy.com/user/maximilian-schwarzmuller/) Udemy course demonstrating the implementation and usage of custom Angular pipes for data transformation.

## Project Overview

This application displays current and historic temperatures for various cities, showcasing Angular's pipe functionality for data formatting and transformation. The project demonstrates both built-in and custom pipe implementations.

## Features

- **Temperature Conversion**: Custom pipe for converting between Celsius and Fahrenheit
- **Sorting Functionality**: Custom impure pipe for sorting arrays
- **Date Formatting**: Built-in Angular DatePipe implementation
- **Real-time Display**: Shows current temperatures for multiple cities
- **Historic Data**: Displays and sorts historic temperature readings for Berlin

## Custom Pipes

### TemperaturePipe (`temp`)
Converts temperature values between Celsius and Fahrenheit with proper formatting.

**Usage:**
```html
{{ temperature | temp: 'cel' : 'fah' }}
```

**Parameters:**
- `value`: Temperature value (string or number)
- `inputType`: 'cel' or 'fah' (input temperature unit)
- `outputType`: 'cel' or 'fah' (desired output unit)

### SortPipe (`sort`)
Sorts arrays in ascending or descending order. Marked as `pure: false` to detect array mutations.

**Usage:**
```html
{{ array | sort: 'asc' }}
```

**Parameters:**
- `value`: Array of strings or numbers
- `direction`: 'asc' or 'desc' (default: 'asc')

## Technologies Used

- Angular (Standalone Components)
- TypeScript
- HTML5
- CSS3

## Cities Featured

- **New York** - Temperature in Celsius
- **Berlin** - Temperature in Celsius
- **Paris** - Temperature in Fahrenheit
- **Chicago** - Temperature in Celsius

## Learning Outcomes

This project demonstrates:
- Creating custom pipes in Angular
- Understanding pure vs impure pipes
- Using built-in Angular pipes (DatePipe, DecimalPipe)
- Data transformation in templates
- Standalone component architecture
- Temperature conversion algorithms

## Installation & Setup

1. Clone the repository
2. Install dependencies:
   ```bash
   npm install
   ```
3. Run the development server:
   ```bash
   ng serve
   ```
4. Navigate to `http://localhost:4200/`

## Course Information

This project was created as part of Maximilian Schwarzmüller's Angular course on Udemy, focusing on pipes and data transformation techniques.

## License

This is a learning project created for educational purposes.
