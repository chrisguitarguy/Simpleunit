# Simple Unit

The simplest PHP unit testing framework. Uses only the PHP core and a little
script.

### Writing Tests

create a directory called `tests` (or something else, more on that later). In
the `tests` directory put files with names separated by underscores that
describe what exactly the file is meant to be test. All test files should end
with `_test.php`. See the `tests` directory in this repo examples.

Each file should, as you may have guessed, test a specific feature. Use PHP's
[`assert`](http://php.net/manual/en/function.assert.php) function to verify
expressions evaluate to true. Be sure to specify the second argument of assert
to get nicer error messages.

    <?php
    assert(1 == 1, "One does not equal one, something is horribly wrong.");

Once your tests are ready, run the `simpleunit` script.

    shell$ ./path/to/simpleunit

### Custom Test Directory

    shell$ TESTS_DIR=path/to/custom/test/dir ./path/to/simpleunit

### Bootstrap Files

    shell$ TESTS_BOOTSTRAP=vendor/autoload.php ./path/to/simpleunit

## Should I Use This?

No, probably not. [PHPUnit](http://phpunit.de/) is probably what you want. This
is to demostrate that automated testing is not much more than just that:
automated. A big framework isn't necessary, but it sure is nice.

## License: MIT

Copyright (c) 2014 Christopher Davis

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
