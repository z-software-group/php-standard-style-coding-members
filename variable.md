variable
========

naming conventions
------------------
 1. full format.                            parable `$camelCaseName_camelCaseAttrib...camelCaseAttrib`
 2. only letter is valid characters naming. code `^([a-zA-z])+$`
 3. name is reagents of variable content.   code `$age = 21;`
 4. naming mode is camelCase.               code `$camelCaseModeUsageForNaming = ':)';`
 5. use attribute in naming:
    - use underscore(_) for separation.     parable `$name_attribute` 
    - numeric attributes:
        ```
        # code

        $user_1 = 'Julie';
        $user_2 = 'Michael';
        ```
    - type attibutes:
        ```
        # code

        $age_int    = 21;
        $age_string = "21";
        ```
    - multi attribute:
        ```
        # code

        $userAge_1_int = 21;
        $userAge_2_int = 35;
        ```

use in coding
-------------
 1. for separating the variables and values from operators ever using space character:
    ```
    # code

    // to max line length 80 character
    $result = $max + 22 + $avarage + $current + $min;

    // if line length over 80 character then use multi-line mode
    $result = $max
            + 22
            + $avarage
            / $current
            * $min;
    ```
 2. use in-line-converter for unification in variables types:
    ```
    # code

    // convert to integer
    $result = 14 + (int)$bool + $max + (int)$string + (int)$float + 56 + $min;

    // convert to boolean
    $result = (bool)$int ? 'YES' : 'NO';

    // convert to string
    $message = "Welcome {$username}, Your last login was " . (string)$userLastLoginDaysAgo . " days ago";
    ```