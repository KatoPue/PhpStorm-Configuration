# Configuration

- https://laravel-news.com/phpstorm-tips-and-tricks
- https://github.com/knpuniversity/phpstorm-settings
- https://github.com/fprochazka/phpstorm-livetemplates/blob/master/Doctrine.xml

| Path                                      | Setting                                          | Value                                           |
| ----------------------------------------- | ------------------------------------------------ | ----------------------------------------------- |
| Editor \| General                         | `Show virtual space at file bottom`              | true                                            |
| Editor \| General \| Appearance           | `Show method separators`                         | true                                            |
| Editor \| General \| Smart Keys           | `Surround selection on typing quote or brace`    | true                                            |
| Editor \| General \| Code folding         | everything, but `PHP class body` and `PHP tags`  | true                                            |
| Editor \| File Encodings                  | `Project Encoding`                               | UTF-8                                           |
| Languages & Frameworks \| PHP \| Composer | `'composer' executable`                          | `C:\ProgramData\ComposerSetup\bin\composer.bat` |

## Keymap for keyboards without numpad (like laptops)

| Path                                                       | Value                    |
| ---------------------------------------------------------- | ------------------------ |
| Keymap \| Main Menu \| Code \| Folding \| Expand           | added `ctrl+plus`        |
| Keymap \| Main Menu \| Code \| Folding \| Expand All       | added `ctrl+shift+plus`  |
| Keymap \| Main Menu \| Code \| Comment with Block Comment  | added `ctrl+alt+shift+7` |

## Code style

`Symfony2` with additions:

| Setting                                                                                            | value                         |
| -------------------------------------------------------------------------------------------------- | ----------------------------- |
| Code Style \| Line separator (for new files)                                                       | Unix and OS X (\n)            |
| Code Style \| PHP \| Wrapping and Braces \| Function declaration parameters                        | Do not wrap                   |
| Code Style \| PHP \| Wrapping and Braces \| Assigment statement \| Align consecutive assignments   | true                          |
| Code Style \| PHP \| Wrapping and Braces \| Class field/constant groups \| Align fields in columns | true                          |
| Code Style \| PHP \| Wrapping and Braces \| Class field/constant groups \| Align constants         | true                          |
| Code Style \| PHP \| Wrapping and Braces \| Array initializer \| Align key-value pairs             | true                          |

## customize the php file header

Go to `File | Settings | Editor | File and Code Templates | Includes | PHP File Header` and add the following or whatever you like:

~~~ php
declare(strict_types=1);

/**
 * This file is part of ${PROJECT_NAME}.
 * (c) author name <author_email@gmail.com>
 *
 * For the full copyright and license information, please view the LICENSE
 * file that was distributed with this source code.
 */

~~~
With this you can change the copyright/license without touching each file in the project.

https://blog.jetbrains.com/phpstorm/2016/11/project-wide-php-7-strict-types-in-phpstorm-2016-3/
https://blog.jetbrains.com/phpstorm/2016/12/updating-your-templates-in-phpstorm/

Go to `File | Settings | Editor | File and Code Templates | Includes | PHP Function Doc Comment` and add the following or whatever you like:
~~~ php
/**
${PARAM_DOC}
 * @return ${TYPE_HINT}
${THROWS_DOC}
*/
~~~
removed check for void ${TYPE_HINT}

## Local PHP Interpreter

Download and install php the way it fits your needs. 
I prefer the method described here over the remote interpreter. For remote interpreters to work correctly, you need to configure folder mapping.
Additionally it takes much more time for the IDE to connect to the VM an run php than running an local interpreter.
Also there is no autosuggest for tools like composer os symfony based console apps.

| Setting                                                             | Value                                           |
| ------------------------------------------------------------------- | ----------------------------------------------- |
| Languages & Frameworks \| PHP \| interpreter                        | define path to your php binary                  |

## Composer as global Command line tool

To get the best out of composer i love to use it as command line tool. To get the arguments and options suggested is a nice thing to have.

| Setting                                                | Value                                                     |
| ------------------------------------------------------ | --------------------------------------------------------- |
| File \| Settings \| Tools \| Command Line Tool Support | Add the new tool of type composer and define it as global |
