# Templar filters

Filters are used to process the result of an expression in a template.

## Overview

As an example, the expression `{{ 'hello' | upper }}` uses the "upper" filter to create
the upper case result "HELLO".

## Built in filters

- require: Will throw an error if the result is empty or null
- default(any): Replaces empty, null, or error types with the default value from the args
- length: Returns the length of a string or array
- lower: Lowercase the rendered result
- upper: Uppercase the rendered result
- trim: Trim whitespace off the rendered result
- split(str?): Split a string into an array. Delimited by newline, but an arg can be used to override the delimiter.
- index(int): Retrieve the int index from the array
- join(str?): Join an array with the provided string. Defaults to newline
- string: Forces the result into a string type, usually by rendering it
- key(str): Retrieve the value of the specified key from the dictionary
- escape_html: (alias 'e') Render the result and escape HTML characters
- yaml: (alias yml) Serialize the data into a YAML string. Requires"yaml-extension" feature (default on)
- json(str?): Serialize the data into a JSON string. Set str to 'pretty' to print with indentation. Requires the "json-extension" feature (default on)
- base64(str?): Encode the result as Base64. If the optional string parameter is set to "decode" then it will try to decode instead. Requires "base64-extension" feature (default on)
