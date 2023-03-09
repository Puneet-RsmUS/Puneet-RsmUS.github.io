# PuneetTestingFile

```Apex
Account a = new Account();
a.name = 'Test Account';
insert accList;

date tomorrow = System.today() + 1;
for (Integer j = 0; j < 10; j++) {
	Opportunity op = new Opportunity();
	op.name = a.name + ' Opportunity ' + j;
	op.StageName = 'Open';
	op.Job_Type__c = 'Active';
	op.CloseDate = tomorrow;
	op.AccountId = a.Id;
	op.RecordTypeId = recordtypeId;
	oppList.add(op);
  }
try {
// Perform the insert operation
insert oppList;
System.debug('Insert operation was successful');
} catch (DmlException e) {
// Handle any exceptions that occur during the insert operation
System.debug('Insert operation failed: ' + e.getMessage());
}
```
