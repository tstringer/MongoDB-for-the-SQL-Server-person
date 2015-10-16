# Learn MongoDB by Examples

*Learn MongoDB  through examples*

- [create test data](/test-data/test-data.js)

## Set database context

#### MongoDB (shell)

```javascript
use yourDatabase;
```

## Read entire collection

#### MongoDB (shell)

```javascript
db.myCollection.find();

// or for prettified output
db.myCollection.find().pretty();
```

## Read certain fields from the collection

#### MongoDB (shell)

```javascript
db.myCollection.find({}, { firstName: 1, lastName: 1 }); // .pretty()

// and to NOT select the default _id field
db.myCollection.find({}, { _id: 0, firstName: 1, lastName: 1 }); // .pretty()
```

## Update document(s) with search predicate

#### MongoDB (shell)

```javascript
db.myCollection.update(
    { lastName: 'Stringer' }, 
    { 
        $set: { 
            firstName: 'Thomas' 
        } 
    }
);
```