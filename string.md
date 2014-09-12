string
======

quote string
------------
 1. to create a plain-string using single-quotes. char `'`
    ```
    #code

    // sample string
    $string = 'hello world!';
    ```
 2. to create a string literals containing apostrophes and variables. char `"`
    ```
    #code

    // apostrophes string
    $sql = "SELECT `table`.* FROM `database`.`table` WHERE `table`.`col` = '{$value}'";
    ```
 3. variables in string. code `$message = "Welcome {$username}";`
 4. strings connection
    ```
    #code

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
 5. ever use the gettext-function to view
    ```
    #code

    #1 example
    $message = gettext('hello world!');

    #2 example
    $welcomeUser = _("Welcome {$username}");
    ``` 