# Logical Components

The logical components are the high level building blocks that compose your vision on the software architecture. Consider it to be your "rough sketch" of the proposed architecture. Thinking about services is too detailed at this stage, so try to think of functionalities that can be isolated into core building blocks: "things that the system needs to do". 

Example: when designing an eCommerce solution, the logical components could be:
**Users**: customer, order processor, sales manager, logistics manager, pick&pack employee
**Building blocks**: Product Catalog, Payments Processor, Order Management, Stock Management, Customer Service, Checkout, Storefront

Do not include details like databases, web services, etc. but focus on the users, roles, building blocks and the interactions between them instead. In the following phase, these building blocks might or might not be turned into services or API's.
