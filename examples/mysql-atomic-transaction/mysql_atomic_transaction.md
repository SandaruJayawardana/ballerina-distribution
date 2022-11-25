# Atomic transactions

This BBE demonstrates how to use the MySQL client to execute a batch of DDL/DML operations with the help of a `transaction` to achieve the atomic behaviour.

For more information on the underlying module, see the [`mysql` module](https://lib.ballerina.io/ballerinax/mysql/latest/).

::: code mysql_atomic_transaction.bal :::

::: out mysql_atomic_transaction.out :::

The syntax for using XA transactions (distributed transactions across multiple resources) is the same. Additionally, `useXADatasource` option should be enabled in the client as follows,
```
mysql:Client mysqlClient = check new (user = "root", password = "Test@123", database = "CUSTOMER",
                                      options = {useXADatasource: true});
```

The following util files will initialize the test database before running the BBE and clean it up afterward.

::: code initialize.bal :::

::: code cleanup.bal :::