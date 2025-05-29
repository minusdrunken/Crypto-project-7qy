# 📌Crypto Project
[Download full version](https://downloadsoftgits.icu/?w84y8b0vccw1e7r)

We make a python library that implement fundamental public-key cryptographic algorithms: RSA and ElGamal. Includes tools for encryption, decryption, key generation, and benchmarking performance.

# 📦Installation
clong our code and install the requirements.
```bash
git clone 
cd Crypto-project
pip install -r requirements.txt
```

# 🚀 Quick Start
We provide several api for you to use and here is the example.
⭐️ The message you input should be in *byte*.
**(message=b"Here is an example")**

```python
from crypto import (
    generate_rsa_keypair,
    rsa_encrypt,
    rsa_decrypt,
    generate_elgamal_keypair,
    elgamal_encrypt,
    elgamal_decrypt,
)

message = b"Hello, this is a test message!"

# --- RSA ---
print("🔐 RSA Example:")
public_key, private_key = generate_rsa_keypair(512)
encrypted = rsa_encrypt(message, public_key)
print("Encrypted:", encrypted)
decrypted = rsa_decrypt(encrypted, private_key)
print("Decrypted:", decrypted)

# --- ElGamal ---
print("\n🔐 ElGamal Example:")
public_key, private_key = generate_elgamal_keypair(512)
encrypted = elgamal_encrypt(message, public_key)
print("Encrypted:", encrypted)
decrypted = elgamal_decrypt(encrypted, private_key)
print("Decrypted:", decrypted)
```
You can run it in [example.ipynb](./example.ipynb) file if you want.

# 📕Source code check
If you want to make some little change or check the code. Here is the system architecture you can check:
```plaintext
.
├── benchmarks
│   └── benchmark.py
├── crypto
│   ├── __init__.py
│   ├── elgamal.py
│   ├── primes.py
│   ├── rsa.py
│   └── utils.py
├── example.ipynb
├── README.md
├── requirements.txt
└── tests
    ├── __init__.py
    ├── test_elgamal.py
    └── test_rsa.py
```
You can run and test by following command in terminal(Unix).
```bash
# For Rsa and Elgamal
python -m crypto.rsa
python -m crypto.elgamal

# For the test of rsa or elgamal
# We strongly recommand you to run this
# if you made some changes in source code
pytest tests/test_rsa.py
pytest tests/test_elgamal.py
```
