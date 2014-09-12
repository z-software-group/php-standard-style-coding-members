if, else and else-if
====================

implementation
--------------
 1. sample if
    ```
    # code

    // one-line comment for describe the condition
    if (condition) {
        // content 4 space to forward
        code
    }

    // after end-bracket a new-line for separator
    ```
 2. sample if-else
    ```
    # code

    // one-line comment for describe the condition
    if (condition) {
        // content 4 space to forward
        code
    } else {
        // content 4 space to forward
        code
    }

    // after end-bracket a new-line for separator
    ```
 3. samole if-elseif-else
    ```
    # code
    // one-line comment for describe the condition
    if (condition) {
        // content 4 space to forward
        code
    } else if (condition) {
        // content 4 space to forward
        code
    } else {
        // content 4 space to forward
        code
    }

    // after end-bracket a new-line for separator
    ```

conditions
----------
 1. conditions converted to boolean
    ```
    # code

    #1 example
    // convert variable type
    if ((bool)$value_int) {
        code
    }

    #2 example
    // convert function return
    if ((bool)function_string()) {
        code
    }
    ```
 2. composition of conditions
    ```
    # code

    #1 example
    // linear combination, to max line length 80 character
    if ($value_bool && (bool)$value_int || function_bool() && (bool)function_int()) {
        code
    }

    #2 example
    // use multi line mode for more 80 character 
    if ($value_bool
     && (bool)$value_int
     || function_bool()
     && (bool)function_int()) {
        code
    }
    ```
 3. parentheses
    ```
    # code

    #1 example
    // muste be use multi line mode
    if (($value_bool
      || (bool)$value_int)
     && (function_bool()
      && (bool)function_int())) {
        code
    }
    ```
 4. reduce the complexity
    ```
    # code

    // simplifying conditions
    $condition_1 = $value_bool || (bool)$value_int;
    $condition_2 = function_bool() && (bool)function_int();

    // understand
    if ($condition_1 && $condition_2) {
        code
    }
    ```