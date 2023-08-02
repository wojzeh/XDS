# XDS
Example of Extensible Data Security (XDS) policies in Microsoft D365FO
## Business case: 
a user can see those purchase orders and their related confirmations only if he or she is Requester. 

## Explanation:
The whole project can basically contain three objects: role, query, and policy.

After creating a specific security role, we need to create a query with HCMWorker table so that it is filtered for the current user.

All constrained tables should be added to the policy by referencing a particular relation (PurchTable, for example, has two relations with HCMWorker table; thus, we need to pick up the required one related to Requester field)

## Note: 
we can create a join expression if a required relation does not exist for a given table.

Once the project built and synchronized, we can assign this new role along with some standard ones to a user. 









