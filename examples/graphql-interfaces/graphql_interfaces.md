# 

A GraphQL schema can have interface types. Then, the other object types can implement the interfaces. All the types that are implementing an interface must consist of the common set of fields defined in the interface type.

In Ballerina, `distinct` `service` classes are used to define interfaces and to define objects that are implementing the interfaces. The Ballerina type inclusions are used to mark an object as an interface implementation.

For more information on the underlying package, see the [GraphQL package](https://lib.ballerina.io/ballerina/graphql/latest/).

::: code graphql_interfaces.bal :::

Run the service by executing the following command.

::: out graphql_interfaces.server.out :::

Invoke the service as follows.

::: out graphql_interfaces.client.out :::