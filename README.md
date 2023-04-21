# version manager
In this TDD kata we are going to mimic a **software versioning system**. 
You have to implement a VersionManager class step by step. Important during this kata is that you have te **write the tests first**. Always start as simple as possible.

VERSION MANAGER SETUP
---------------------

1. Create a constructor that takes an optional parameter, as a String. This will represent the initial version. 
* The input will be in one of the following formats: "{MAJOR}", "{MAJOR}.{MINOR}", or "{MAJOR}.{MINOR}.{PATCH}".
* Start with the most simple test case with only a major version, and move to major.minor and finally major.minor.patch.
***


2. Values added after PATCH should be ignored. 
* More values may be provided after PATCH but they should be ignored
* "{MAJOR}.{MINOR}.{PATCH}.40" becomes "{MAJOR}.{MINOR}.{PATCH}"
* Test first!
***


3. The first three parts should be decimal.
* If these 3 parts are not decimal values, an exception with the message "Error occured while parsing version!" should be thrown.
* "{MAJOR}.b.{PATCH}" should throw an exception.
* Try to write tests for multiple cases.
***


4. Use a default version.
* If the initial version is not provided or is an empty string, use "0.0.1" by default.
***


MAJOR - MINOR - PATCH - ROLLBACK
--------------------------------
This class should support a patch, minor, major and rollback method, all of which should be chainable

5. version can increase the PATCH version
* increase the patch number by 1.
***


6. version can increase the MINOR version.
* increase the minor version by 1.
* set the patch version to 0.
***


7. version can increase the MAJOR version
* increase the major version by 1.
* set the patch and minor version to 0.
***


8. rollback versions
* return the MAJOR, MINOR, and PATCH to their values before the previous major/minor/patch call.
* multiple calls to rollback() should be possible and restore the version history.
***


9. no version to roll back to
* throw an exception with the message "Cannot rollback!" if there's no version to roll back to
***


RELEASE
-------
10. release a version
* return a string in the format "{MAJOR}.{MINOR}.{PATCH}"
