# Str - UTF-8 Chainable String Manipulation

## 📝 Description
The `Str` class is a chainable, UTF-8 compatible string manipulation utility built on top of `TUTF8`. It provides a clean and efficient API for processing strings, supporting a wide range of operations without requiring external calls to retrieve results.

### 🌍 Languages Supported
- Full UTF-8 support for multilingual strings.
- Methods optimized for performance and readability.

## 🚀 Features
- **UTF-8 Support**: Built on `TUTF8` for reliable handling of Unicode strings.
- **Chainable Methods**: Enables fluent and readable code.
- **Comprehensive String Operations**: From trimming to slug creation, covering all common string manipulations.
- **Multibyte Safe**: Handles multibyte characters correctly.

## 📌 Installation
Include the `Str` class in your project via Composer or by directly integrating the `ASCOOS\FRAMEWORK\Kernel\Strings\Str` namespace.

```bash
composer require ascoos/framework
```

## 📖 Usage Examples
```php
use ASCOOS\FRAMEWORK\Kernel\Strings\Str;

// Basic string manipulation
echo Str::of('  Ascoos Text  ')
    ->trim()
    ->upper()
    ->slug('-', false); // Output: ASCOOS-TEXT

// Check if string contains a substring
if (Str::of('Hello World')->contains('World')) {
    echo "The word exists!";
}

// Replace a substring
echo Str::of('Hello World')->replace('World', 'GitHub'); // Output: Hello GitHub

// Extract a substring
echo Str::of('This is a long text')->substr(0, 10); // Output: This is a
```

## 🔧 Methods
The following table lists all available methods in the `Str` class with their descriptions:

| Method | Description |
|--------|-------------|
| `__construct(string $string)` | Initializes the `Str` instance with the given string. |
| `get(): string` | Retrieves the processed string. |
| `casecmp(string $string): int` | Performs a binary-safe, case-insensitive string comparison. |
| `cmp(string $string): int` | Performs a multibyte binary-safe string comparison. |
| `contains(string $needle): bool` | Checks if the string contains the specified substring. |
| `cspn(string $characters, int $offset = 0, ?int $length = null): int` | Finds the length of the initial segment not matching a mask. |
| `cut(int $start, ?int $length = null): string` | Cuts the string at the specified position and length. |
| `endsWith(string $needle): bool` | Checks if the string ends with the specified substring. |
| `implode(string $separator, array $array): string` | Joins array elements into a string with a specified separator. |
| `ireplace(string $search, string $replace, int &$count = null): string\|array` | Performs case-insensitive string replacement. |
| `lcfirst(): string` | Converts the first character of the string to lowercase. |
| `lower(): string` | Converts the entire string to lowercase. |
| `ltrim(): string` | Removes whitespace from the beginning of the string. |
| `of(string $string): self` | Creates a new `Str` instance. |
| `ord(): int\|false` | Returns the Unicode code point of the first character. |
| `pad(int $length, string $pad_string = " ", int $pad_type = STR_PAD_RIGHT): string` | Pads the string to a specified length with a given string. |
| `parse_str(array &$result): bool` | Parses the string into variables. |
| `repeat(int $times): string` | Repeats the string a specified number of times. |
| `replace(string $search, string $replace): string` | Replaces occurrences of a substring. |
| `rtrim(): string` | Removes whitespace from the end of the string. |
| `scrub(): string` | Removes invalid characters from the string. |
| `slug(string $separator = '-'): string` | Converts the string into a slug format. |
| `split(string $pattern, int $limit = -1): array\|false` | Splits the string using a regular expression. |
| `startsWith(string $needle): bool` | Checks if the string starts with the specified substring. |
| `str_split(int $length = 1): array` | Splits the string into an array of characters or chunks. |
| `strimwidth(int $start, int $width, string $trim_marker = ""): string` | Trims the string to a specified width. |
| `strip(): string` | Strips high-byte characters to return a pure 7-bit ASCII string. |
| `stripos(string $needle, int $offset = 0): int\|false` | Finds the position of the first occurrence of a substring (case-insensitive). |
| `stristr(string $needle, bool $before_needle = false): string\|false` | Finds the first occurrence of a substring (case-insensitive). |
| `strlen(): int` | Returns the length of the string. |
| `strncmp(string $string, int $length): int` | Compares the first n characters of two strings. |
| `strpos(string $needle, int $offset = 0): int\|false` | Finds the position of the first occurrence of a substring. |
| `strrchr(string $needle, bool $before_needle = false): string\|false` | Finds the last occurrence of a character and returns the substring. |
| `strrev(): string` | Reverses the string. |
| `strrichr(string $needle, bool $before_needle = false): string\|false` | Finds the last occurrence of a character (case-insensitive). |
| `strripos(string $needle, int $offset = 0): int\|false` | Finds the position of the last occurrence of a substring (case-insensitive). |
| `strrpos(string $needle, int $offset = 0): int\|false` | Finds the position of the last occurrence of a substring. |
| `strspn(string $characters, int $offset = 0, ?int $length = null): int` | Finds the length of the initial segment matching a mask. |
| `strstr(string $needle, bool $before_needle = false): string\|false` | Finds the first occurrence of a substring. |
| `strwidth(): int` | Calculates the width of the string. |
| `substr(int $start, ?int $length = null): string` | Extracts a portion of the string. |
| `substr_count(string $needle): int` | Counts the number of substring occurrences. |
| `substr_replace(string $replace, int $offset, int\|null $length = null): string` | Replaces a portion of the string. |
| `trim(): string` | Removes whitespace from both ends of the string. |
| `ucfirst(): string` | Converts the first character of the string to uppercase. |
| `ucwords(?string $separators = null): string` | Uppercases the first character of each word. |
| `upper(): string` | Converts the entire string to uppercase. |

## 📜 License
This project is licensed under the [**AGL-F**](LICENSE_AGL-F.md) license.

---