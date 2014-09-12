string
======

quote string
------------
 1. create a normal-string by use of single-quotes. char `'`
    ```
    # code

    // sample string
    $string = 'hello world!';
    ```
 2. create a string literals containing apostrophes and variables by use of double-quotes. char `"`
    ```
    # code

    // apostrophes string
    $sql = "SELECT `table`.* FROM `database`.`table` WHERE `table`.`col` = '{$value}'";
    ```

use in coding
-------------
 1. variables in string. code `$message = "Welcome {$username}";`
 2. strings connection
    ```
    # code

    #1 example
    // for max line length 80 character
    $message = "Welcome {$username}" . ', Your last login was ' . (string)$userLastLoginDaysAgo_int . ' days ago';

    #2 example
    // use multi line mode
    $sql = "SELECT `table`.* "
         . "FROM `database`.`table` "
         . "WHERE `table`.`col` = '{$value}' "
         . "LIMIT 30, 1";
    ```
 3. ever use the gettext-function to view
    ```
    # code

    #1 example
    // use gettext
    $message = gettext('hello world!');

    #2 example
    // use _ replace gettext
    $welcomeUser = _("Welcome {$username}");
    ```
 4. as function arguments, do not break the string
    ```
    # code

    // the long string
    throw new Exception(_('this is a very very very very very very very very very very very very very very very very very long'));
    ``` 