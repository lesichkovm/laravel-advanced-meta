# Laravel Advanced Meta

A meta solution for Laravel for advanced users. Allows to add custom metas (key value pairs) to any object.

## Benefits ##

- The meta tags be attached to any object, as long as it has a unique object identifier.
- The meta value is converted to JSON, allowing it to hold arrays

## Usage ##

- Copy the Meta model to your models directory.
- Create the meta table manually, or use the tableCreate method in the Meta model
```
  Id (VARCHAR 40)
  ObjectId (VARCHAR 40, INDEX)
  Key (VARCHAR 255, INDEX)
  Value (LONGTEXT) - Holds JSON values
  CreatedAt (DATETIME, NULLABLE)
  UpdatedAt (DATETIME, NULLABLE)
  DeletedAt (DATETIME, NULLABLE)
 ```
- Change anything to suit your work style (table name, column names, etc)
  
## ObjectId ##

Your Models should already use UUID, GUID, or other UID (unique identifier) instead of auto incremental IDs.

If you still use auto incremental ids, this is fine. You can still create an ObjectId using the following pattern: ObjectType + Id = ObjectTypeId (i.e. User12, Post42, Email32, etc)

Piece of advice, if you are not using really unique identifiers for your models, please do so.
