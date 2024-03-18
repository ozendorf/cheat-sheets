# Python Security Cheat Sheet

## 1. Password Hashing with hashlib

```python
import hashlib

# Generate a SHA-256 hash of a password
password = "secret"
hashed_password = hashlib.sha256(password.encode()).hexdigest()
```

## 2. Symmetric Encryption with cryptography

```
from cryptography.fernet import Fernet

# Generate a symmetric encryption key
key = Fernet.generate_key()

# Initialize a Fernet cipher with the key
cipher = Fernet(key)

# Encrypt a message
message = "sensitive data"
encrypted_message = cipher.encrypt(message.encode())

# Decrypt the encrypted message
decrypted_message = cipher.decrypt(encrypted_message).decode()
```
# 3. Asymmetric Encryption with cryptography

```
from cryptography.hazmat.backends import default_backend
from cryptography.hazmat.primitives import serialization
from cryptography.hazmat.primitives.asymmetric import rsa
from cryptography.hazmat.primitives.asymmetric import padding

# Generate an RSA key pair
private_key = rsa.generate_private_key(
    public_exponent=65537,
    key_size=2048,
    backend=default_backend()
)
public_key = private_key.public_key()

# Encrypt a message with the public key
message = "sensitive data"
encrypted_message = public_key.encrypt(
    message.encode(),
    padding.OAEP(
        mgf=padding.MGF1(algorithm=hashes.SHA256()),
        algorithm=hashes.SHA256(),
        label=None
    )
)

# Decrypt the encrypted message with the private key
decrypted_message = private_key.decrypt(
    encrypted_message,
    padding.OAEP(
        mgf=padding.MGF1(algorithm=hashes.SHA256()),
        algorithm=hashes.SHA256(),
        label=None
    )
).decode()
```

# 4. Secure Random Number Generation with secrets
```

import secrets

# Generate a secure random integer
secure_random_integer = secrets.randbelow(1000)
```


# 5. Timing-Safe Comparison of Strings
```

import hmac

# Timing-safe comparison of two strings
def secure_compare(s1, s2):
    return hmac.compare_digest(s1, s2)

```
# 6. Secure File Permissions
```
import os

# Set secure file permissions (readable only by owner)
os.chmod("file.txt", 0o600)

```
# 7. Secure Input Handling with getpass
```

import getpass

# Prompt user for a password without echoing input
password = getpass.getpass("Enter your password: ")

```
# 8. Secure Error Handling with try-except
```
# Secure error handling to prevent information leakage
try:
    # Code that may raise an exception
    pass
except Exception as e:
    # Handle the exception securely
    pass
```

# 9. Sanitize User Input with bleach
```
import bleach

# Sanitize user input to remove potentially dangerous content
sanitized_input = bleach.clean(user_input)
```

# 10. Secure Logging with logging
```
import logging

# Configure secure logging settings
logging.basicConfig(filename='app.log', level=logging.INFO)
```
