# AuthoRex

AuthoRex is a Python package for generating and authenticating OTPs (One-Time Passwords) using MongoDB for storage. This package is useful for applications that require secure OTP-based authentication.

## Features

- Generate OTPs.
- Authenticate OTPs.
- Uses MongoDB for storing OTPs securely.

## Installation

You can install AuthoRex using pip:

```sh
pip install AuthoRex
```

## Usage

### Importing the package

You can import the entire package or specific functions:

```python
import AuthoRex

# Or import specific functions
from AuthoRex import genOTP, authOTP
```

### Generating an OTP

Generate an OTP for a given number:

```python
# Using the package import
print(AuthoRex.genOTP("123"))

# Using the function import
print(genOTP("123"))
```

### Authenticating an OTP

Authenticate an OTP for a given number:

```python
# Using the package import
print(AuthoRex.authOTP("123", 123456))  # Replace 123456 with the actual OTP generated

# Using the function import
print(authOTP("123", 123456))  # Replace 123456 with the actual OTP generated
```

## Example

Here's a complete example of how to use AuthoRex:

```python
import AuthoRex

# Generate OTP for a number
response = AuthoRex.genOTP("123")
print(response)

# Authenticate OTP for the same number
is_authenticated = AuthoRex.authOTP("123", 123456)  # Replace 123456 with the actual OTP generated
print("Authenticated" if is_authenticated else "Authentication Failed")
```

## MongoDB Configuration

AuthoRex uses MongoDB to store OTPs. Make sure you have a MongoDB instance running and update the MongoDB URI in the code as per your setup.

## License

This project is licensed under the Creative Commons Attribution-ShareAlike 4.0 International License. See the [LICENSE](https://github.com/TraxDinosaur/AuthoRex/blob/main/LICENSE) file for more details.

## Author

AuthoRex is developed and maintained by [TraxDinosaur](https://github.com/TraxDinosaur). For any queries or support, you can reach out to [TraxDinosaur](https://traxdinosaur.github.io).

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request for any improvements or bug fixes.

## Acknowledgements

- The package uses [pymongo](https://pypi.org/project/pymongo/) for MongoDB interactions.
