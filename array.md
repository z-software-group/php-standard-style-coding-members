array
=====

create array
------------
 1. create online array and initialization
    ```
    # code

    // initialization
    $configs = array();

    // create online array
    $configs['database']['hostname'] = '%hostname';
    $configs['database']['username'] = '%username';
    $configs['database']['password'] = '%password';
    $configs['database']['database'] = '%database';
    ```
 2. keys and values
    ```
    # code

    // to max line length 80 character
    $users = array('julie' => $julie, $guest);

    // use multi line mode
    $users = array('julie'   => $julie,
                   'michael' => $michael,
                   $guest);
    ```
 3. create as function arguments
    ```
    # code

    $db = new Db(array('hostname' => $hostname,
                       'username' => $username,
                       'password' => $password,
                       'database' => $database));
    ```