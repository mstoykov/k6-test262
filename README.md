# This a WIP 
The point of this repo is to test k6 goja+babel+core.js combo against the tc39 test suite.

Ways to use it:
1. Checkout test262 in testdata directory
2. Run `go test &> out.log` 

if there are failures there will be a JSON with what failed. 
The full list of failing tests is in `breaking_test_errors.json` in order to regenerate it (in case
of changes) it needs to become an empty JSON object `{}` and then the test should be rerun and the
new json should be put there.

TODO:
1. enable more test currently only es5 and es6 tests are enabled but babel supports some ES2016 and
   ES2017 
2. disable tests that we know won't work and .. don't care
3. Make this faster and better 
4. Move it to inside k6
