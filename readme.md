# VerifyKit

VerifyKit is the next gen phone number validation system. Users can easily verify their  phone numbers without the need of entering phone number or a pin code.

## Requirements

 - Node 6 +

## Installation

You can install npm package

```bash
npm install VerifyKit
```


## Usage

```javascript
const VerifyKit = require('./VerifyKit.js')

const verifyKit = new VerifyKit("server_key");

verifyKit.validate('session_id').then(response => {
    console.log('Success');
}).catch(error => {
    console.log('Verification Failed')
});
```

### Validation Success Response
```json
{
    "validationType": "whatsapp",
    "validationDate": "2019-11-07 07:35:28",
    "phoneNumber": "+905555555555"
}
```


### Validation Fail Response
```json
{
  "requestId": "request id",
  "httpStatusCode": 403,
  "errorMessage": "error message",
  "errorCode": "error code"
}
```


## Author

VerifyKit is owned and maintained by [VerifyKit DevTeam](mailto:sdk@verifykit.com).


## License

The MIT License

Copyright (c) 2019-2020 VerifyKit. [http://verifykit.com](http://verifykit.com)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.