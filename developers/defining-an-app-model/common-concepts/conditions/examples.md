# Examples

Examples of conditions are:

| Textual                                  | Logical                               |
|------------------------------------------|---------------------------------------|
| *The customer has a credit card*         | `Customer.Credit Card has value`      |
| *The job application is being processed* | `Job Application.Status = In Process` |

In the first example, the condition is evaluated as **true** if the Customer has a credit card, i.e. it is evaluated based on the existence of an object (Credit Card). In the second example, the condition is evaluated as **true** if the state of the Job Application (the object) is Active, i.e. it is evaluated based on the state of the object.

Examples of conditions on the relationships between objects are:

| Textual                                  | Logical                                                       |
|------------------------------------------|---------------------------------------------------------------|
| *The person has a submitted timesheet*   | `Person.Timesheet exists WHERE Timesheet.Status = Submitted`  |
| *The customer has no accepted contracts* | `Customer.Contract not exists WHERE Contract.Accepted = True` |

These examples are evaluated based on relationships between different objects, and the state or existence of these relationships.

Conditions can be combined, i.e. one might define a logical statement about the state of an object and the relationships to other objects at once. For example:

| Textual                                              | Logical                             |
|------------------------------------------------------|-------------------------------------|
| *The person is active, and has an active assignment* | `Person.State = Active AND Person.Assignment exists WHERE Assignment.State = Active` |

This example combines 2 conditions (*The person is active* and *The person has an active assignment*) into one, separated by the logical `AND` operator, meaning that both conditions has to be fulfilled. These two conditions might also be separated by the logical `OR` operation, meaning that statement is **true** if the person is active, or if the person has an active assignment, or both.