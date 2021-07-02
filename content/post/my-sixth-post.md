---
title: "My Sixth Post"
date: 2021-07-02T16:34:17-05:00
draft: false
---

C# Functions

```c#
public int AddNumbers(int number1, int number2)
{
    int result = number1 + number2;
    if(result > 10)
    {
    return result;
    }
}
```

SQL Example

```sql
CREATE TABLE Persons (
    PersonID int,
    LastName varchar(255),
    FirstName varchar(255),
    Address varchar(255),
    City varchar(255)
);
```

Another SQL
```sql
SELECT Orders.OrderID, Customers.CustomerName, Shippers.ShipperName
FROM ((Orders
INNER JOIN Customers ON Orders.CustomerID = Customers.CustomerID)
INNER JOIN Shippers ON Orders.ShipperID = Shippers.ShipperID);
```

Powershell Example
```ps
write-host("using for loop")
for ($i = 0; $i -le ($myList.length - 1); $i += 1) {
  $myList[$i]
}

write-host("using forEach Loop")
foreach ($element in $myList) {
  $element
}

write-host("using while Loop")
$i = 0
while($i -lt 4) {
  $myList[$i];
  $i++
}
```


Go Example

```go {hl_lines=[8,"15-17"]}
// GetTitleFunc returns a func that can be used to transform a string to
// title case.
//
// The supported styles are
//
// - "Go" (strings.Title)
// - "AP" (see https://www.apstylebook.com/)
// - "Chicago" (see https://www.chicagomanualofstyle.org/home.html)
//
// If an unknown or empty style is provided, AP style is what you get.
func GetTitleFunc(style string) func(s string) string {
  switch strings.ToLower(style) {
  case "go":
    return strings.Title
  case "chicago":
    return transform.NewTitleConverter(transform.ChicagoStyle)
  default:
    return transform.NewTitleConverter(transform.APStyle)
  }
}
```

Step 1: add the ValueTuple nuget package to your project.

Step 2: as Lucas says in his comment, change the syntax to:

```c#
public class Location  
{
     public string City { get; set; }
     public string State { get; set; }

     public Location(string city, string state)
     {
           City = city;
           State = state;
     }
}

// Example
var location = new Location("Lake Charles","LA");  
// Print out the address
var address = $"{location.City}, {location.State}";
```

Kubernetes YAML files

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: nginx-deployment
spec:
  selector:
    matchLabels:
      app: nginx
  replicas: 2 # tells deployment to run 2 pods matching the template
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
      - name: nginx
        image: nginx:1.14.2
        ports:
        - containerPort: 80

```

JSON Exmple

```json
{
    "menu": {
        "id": "file",
        "value": "File",
        "popup": {
            "menuitem": [
                {"value": "New", "onclick": "CreateNewDoc()"},
                {"value": "Open", "onclick": "OpenDoc()"},
                {"value": "Close", "onclick": "CloseDoc()"}
            ]
        }
    }
}
```

XML Content

```xml
<menu id="file" value="File">
  <popup>
    <menuitem value="New" onclick="CreateNewDoc()" />
    <menuitem value="Open" onclick="OpenDoc()" />
    <menuitem value="Close" onclick="CloseDoc()" />
  </popup>
</menu>
```

Python Code Example
```python
class MyNumbers:
  def __iter__(self):
    self.a = 1
    return self

  def __next__(self):
    x = self.a
    self.a += 1
    return x

myclass = MyNumbers()
myiter = iter(myclass)

print(next(myiter))
print(next(myiter))
print(next(myiter))
print(next(myiter))
print(next(myiter))
```

Bash Example
```bash
#!/bin/bash
echo $0      # prints the script name

echo $1      # prints the first argument
echo $2      # prints the second argument
echo $9      # prints the ninth argument
echo $10     # prints the first argument, followed by 0 
echo ${10}   # prints the tenth argument

echo $#      # prints the number of arguments
```