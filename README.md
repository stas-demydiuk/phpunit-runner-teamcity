phpunit-runner-teamcity
======================================

This library features a PHPUnit runner for TeamCity. It makes use of TeamCity service messages to report unit test results directly to TeamCity.

## Installation

### Composer

To add PHPUnit runner for TeamCity as a local, per-project dependency to your project, simply add a dependency on `4you4ever/phpunit-runner-teamcity` to your project's `composer.json` file. Here is a minimal example of a `composer.json` file that just defines a development-time dependency on PHPUnit 3.7:

    {
        "require-dev": {
            "4you4ever/phpunit-runner-teamcity": "dev-master"
        },
        "repositories": [
            {
                "type": "git",
                "url": "https://github.com/4you4ever/phpunit-runner-teamcity.git"
            }
        ],
    }

## Usage

Add new "Command Line" build step to your TeamCity project with script:

```bash
%teamcity.build.checkoutDir%/vendor/bin/phpunit-tc -c %teamcity.build.checkoutDir%/path/to/config.xml %teamcity.build.checkoutDir%/path/to/tests/dir/
```
