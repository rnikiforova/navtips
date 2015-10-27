## Desired result
Update appearance of a field or a row based on some condition.

## How to accomplish it
Create a global boolean variable. Check for it in **OnFormat** in the C\AL of *every* field from a row (No., Description, Description 2).

##Known issues
* The formatting won't be change unless you click on another line and then back again
* You get "Not enough memory" error if you try to fix it with **CurrForm.Update** in **OnFormat**

##  Solution
* Add CurrFormat.Update in **OnAfterValidate**. You should add it to *every* field from the row where you want something to happen in **OnFormat**.

```
OnFormat
---------
IF (Description is empty) THEN
	Description.UpdateForeColor(RED)
ELSE
	Description.UpdateForeColor(BLACK)

OnAfterUpdate
-------------
CurrForm.Update;
```

