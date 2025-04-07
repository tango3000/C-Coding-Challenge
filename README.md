>[!NOTE]
Converts numeric keypad sequences to text (input)
Supports keys 2-9 with standard letter mappings
Requires # terminator for all inputs
Space acts as separator, * is delete function
Requires .NET 6.0+ and basic C# knowledge

>[!WARNING]
Input must end with # or fails
No support for key 1
Multiple spaces may cause unexpected results
Very long sequences wrap around

>[!IMPORTANT]
Must instantiate OldPhonePadConverter
Returns uppercase only
Examples: "4433555 555666#" → "HELLO"
Includes comprehensive test cases

# OldPhonePad Converter

Old Phone Pad Keystroke Converter

## Description

This project implements the `OldPhonePadConverter` class, which translates keystroke sequences from a traditional numeric keypad (like those on older phones) into text messages.

> [!TIP]
- Converts numeric sequences to letters according to the standard
- Supports keys 2 through 9
- Handles spaces as separators
- Implements the asterisk (*) as the delete key
- Requires the hash (#) as a terminator

## Basic Usage

``` csharp
var converter = new OldPhonePadConverter();
string result = converter.Convert("4433555 555666#"); // Returns "HELLO"
```

## Key Mapping

| Key | Letters |
|-------|---------|
| 2 | A B C |
| 3 | D E F |
| 4 | G H I |
| 5 | J K L |
| 6 | M N O |
| 7 | P Q R S |
| 8 | T U V |
| 9 | W X Y Z |

## Usage examples

```csharp
Console.WriteLine(converter.Convert("33#")); //E
Console.WriteLine(converter.Convert("227*#")); //B
Console.WriteLine(converter.Convert("2 22 222#")); // A B C
```

## Requirements

- .NET 6.0 or higher
- Basic knowledge of C#

## Installation

1. Clone the repository
2. Open the solution in Visual Studio
3. Compile the project

## Tests

The project includes test cases for:
- Basic conversions
- Delete key (*)
- Handling spaces
- Edge cases
- Invalid input

## License

MIT License
