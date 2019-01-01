# DEPRECATED

You probably shouldn't use this package, use [the official SDK](https://developers.intercom.com/installing-intercom/docs/intercom-javascript) instead.

---

# Walkie-Talkie
### An interface for speaking to intercom.io API.

Walkie-Talkie is a fork of the original project [node-intercom](https://github.com/silentrob/node-intercom) developed by [Rob Ellis](https://github.com/silentrob).
I used the original project as a basis to further develop my nodeJS skills and contribute back to the Open Source community. We also use Walkie-Talkie internally for [Postach.io](http://postach.io) for recording events and user conversation management.


## Installation

To start playing with the library in your project, run

    npm install walkie-talkie --save


## API Overview

To implement Walkie-Talkie, this is the basic method to get data for a user by email

    var settings = {
      "api_key": "your_API_key",
      "app_id": "your_APP_ID"
    }

    var intercom = require('walkie-talkie').app(settings);

    intercom.users.get('test@example.com', function(code, body) {
        // code is the request status code from the API
        // body is the response body as a JSON object
        console.log(code);
        console.log(body);
    });

See the tests folder for more examples on usage. The Intercom.io complete docs can be found here - http://doc.intercom.io/api/


## Contributing and Testing

Contributing bug fixes and features is very welcome! If you want to contribute to the project, you'll need to create and run tests for anything you add that needs it.

Mocha is used for testing so add your tests to the `test` folder, but first you'll need to create a `config.json` file in the root of the tests folder and fill it with your credentials.

Start by installing the project dependencies by running

    npm install && npm install -g mocha gulp

then create your `config.json` in the `test` folder.

    {
      "settings": {
        "app_id": "APP_ID_HERE",
        "api_key": "API_KEY_HERE"
      }
    }

Now you can finally run the tests.

    gulp test


## TODO

- Companies
- Admins
- Notes
- Conversations


## License

This is a fork of the original project located [here](https://github.com/silentrob/node-intercom). The copyright and license has been maintained.

Copyright 2012 Chloi Inc.
All rights reserved.

Permission is hereby granted, free of charge, to any person
obtaining a copy of this software and associated documentation
files (the "Software"), to deal in the Software without
restriction, including without limitation the rights to use,
copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the
Software is furnished to do so, subject to the following
conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES
OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT
HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,
WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.
