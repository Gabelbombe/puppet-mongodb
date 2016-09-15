#### MongoDB Module

Module for creating a MongoDB server.

##### NOTE: This module is Ubuntu specific.

```puppet
Sample Usage :
  node 'mongodb-1.domain.com', 'mongodb-2.domain.com', 'mongodb-3.domain.com' {
    # Install MongoDB
    class { mongodb:
      # Nodes are in a replica set
      replSet => "example_set_name",
      # Increased open files limit (MongoDB connections, etc.)
      ulimit_nofile => 20000,
    }
}
```
