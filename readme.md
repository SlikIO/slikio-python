This is a python library for [SlikIO](http://slik.io).

# Usage
### Installation
To get the library:
`pip install slikio-python`
###Requires:
* requests

Then, register to [SlikIO](http://slik.io) if you haven't done so already, then get the private API key, and initialize the framework:

```python
import slikio

slikio =  slikio.SlikIO("prvkey_080618f6837fe75d8511")
```

## Pushing data to collections:
To push data to your collection use the `sendData` method:
```python
slikio.sendData(COLLECTION_ID, data);
```
Example:
```python
data = {
	'user_id': '123123',
	'email': 'user@email.com',
	'action': 'planPurchased',
	'cost': 150.0
}

response = slik.sendData("col_3131c141431242", data)
print response.text 
# will print the response body, example: "success":"Data added to collection col_3131c141431242"}
```