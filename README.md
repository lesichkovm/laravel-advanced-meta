# Laravel Advanced Meta

An advanced meta solution for Laravel. 

## Benefits ##

- The meta tags be attached to any object, as long as it has a unique object identifier.
- The meta value is converted to JSON, allowing it to hold arrays

## Usage ##

- Copy the Meta model to your models directory.
- Create the meta table manually, or use the tableCreate method in the Meta model

  Id (VARCHAR 40)
  ObjectId (VARCHAR 40)
  Key (VARCHAR 255)
  Value (LONGTEXT)
  CreatedAt (DATETIME)
  UpdatedAt (DATETIME)
  DeletedAt (DATETIME)
  
- Change anything to suit your work style
  
## ObjectId ##

Your Models should already use UUID, or UID instead of auto incremental IDs.

If you still use auto incremental ids, this is fine. You can still create an ObjectId using the following pattern: ObjectType + Id = ObjectTypeId (i.e. User12, Post42, Email32, etc)

But yes, if you are not using really unique identifiers for your models, please do so.
