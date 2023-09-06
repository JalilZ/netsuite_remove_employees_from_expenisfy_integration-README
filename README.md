# Workato Recipe

Auto remove employees access from expensify</br>
For security measures, I cannot share the .json for this recipe - let me know if you need guidance on this topic !

## Workato actions explained

1. Trigger if netsuite employee is added/created & "Expensify User" is False
3. Prevent removing system admin - this step makes exception that prevents removing system admins from expensify
6. create variables "email_to_remove_from_all_policies" and "data_revoke" (currently empty, both will store the request body: user data that will be removed) and "requestJobDescription_revoke" (stores the request body for the revoke HTTP request)
11-14. Get all policies in expensify, iterate each policy and for each iteration update the "email_to_remove_from_all_policies" and "data_revoke" and send request to remove the user.
15. Stop

## NetSuite ERP

For better automation, this recipe works simultaneously with netsuite workflows that automatically set "Expensify User" as false once the employee termination date is <= today. 

## Author

Jalil

