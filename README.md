# secret-castle-auth

Secure authentication library for managing secrets, leveraging Node.js's built-in `crypto` module for encryption and decryption of sensitive information.

## Installation

Run the following command to install `secret-castle-auth`:

```bash
npm install secret-castle-auth
```

## Usage

First, import `secret-castle-auth` into your project:

```javascript
const SecretCastleAuth = require('secret-castle-auth');
```

Create an instance of `SecretCastleAuth` with your secret key:

```javascript
const secretKey = 'your-secret-key-here'; // Ensure this is securely generated and stored
const sca = new SecretCastleAuth(secretKey);
```

### Encrypting Data

To encrypt data, use the `encrypt` method:

```javascript
const encryptedData = sca.encrypt('Sensitive information');
console.log(encryptedData);
```

### Decrypting Data

To decrypt data, use the `decrypt` method with the output from the `encrypt` method:

```javascript
const decryptedData = sca.decrypt(encryptedData);
console.log(decryptedData); // Outputs: Sensitive information
```

## Contributing

Contributions are welcome! Please submit a pull request or create an issue for any features or bug fixes.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
