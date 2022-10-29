# Request.js
The simplest and lightest Node.js module for sending Post or Get Requests.

<br/>

## Installation
```
npm install @hqdaemon/request
```

## Usage Node.js
The module will try to convert the received information into JSON.
If it fails output Plain Text.

```js

// Import library
const request = require("@hqdaemon/request");

/*

Request Options

*/

let options = {

	/*

	Full requested URL without queries

	*/

	url: "https://example.com",

	/*

	Request Method
	Values: "GET" or "POST"
	Default "POST"

	*/

	method: "GET",

	/*
	
	Query params
	Object or String
	Default {}

	*/

	params: {
		firstParam: "firstValue",
		secondParam: "secondValue"
	},

	/*

	Authorization header
	Default False

	*/

	auth: "AUTH_STRING",

	/*
		Additional Headers
		Default False
	*/

	headers: {
		"-x-your-header-param": "Some value",

		/*

		You can override Content-Type
		Default "application/json"

		*/

		"Content-Type": "application/x-www-form-urlencoded"
	}
};

// Send Request
let result = await request(options);

```

<br />
<br />
<br />
<br />

## MIT License

Copyright (c) Alexander Yermolenko • [surfy.one](https://surfy.one)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.