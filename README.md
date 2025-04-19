# DataUnload

DataUnload is a Java utility library for generating realistic test data for development and testing purposes. It provides a variety of methods to generate random but plausible names, addresses, contact information, dates, and other common data types.

## Features

- **Name Generation**: First names, last names, full names, and genres
- **Address Generation**: Streets, cities, countries, postal codes, time zones
- **Contact Information**: Phone numbers, email addresses, domains, URLs
- **Date/Time Generation**: Birth dates, ages, past/future dates, date ranges
- **Internet Related**: Email addresses, domains, URLs, IP addresses
- **Financial Data**: Prices, currencies, credit card numbers
- **International Support**: Country codes, phone formats, postal code formats

## Installation

1. Clone the repository or download the source files
2. Ensure all data files are in the `src/main/java/data/` directory
3. Include the `DataUnload.java` file in your project

## Usage

Simply call the static methods from the `DataUnload` class:

```java
// Name generation
String firstName = DataUnload.firstName();
String fullName = DataUnload.fullName();

// Address generation
String street = DataUnload.street();
String city = DataUnload.city();
String postalCode = DataUnload.postal("US");

// Contact information
String email = DataUnload.email();
String phone = DataUnload.phone("GB");

// Date generation
LocalDate birthDate = DataUnload.birthDate();
int age = DataUnload.age(birthDate);

// Financial data
double price = DataUnload.price();
String currency = DataUnload.currency();
```

## Notes

- All generated data is random but designed to be plausible
- The library is thread-safe using ThreadLocalRandom
- The class cannot be instantiated (utility class pattern)
- Some methods may throw IllegalArgumentException for invalid inputs

