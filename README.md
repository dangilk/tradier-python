# Tradier-Python

Tradier-python is a python client for interacting with the Tradier API.


## Getting Started

You will need a Tradier account token which you can download from your account after logging in. 

The client also takes an optional default_account_id which can make it easier to get information if you only have one account. 

The default endpoint is the sandbox. You will need to set the endpoint to the brokerage endpoint for live use. 

Reference documentation for the API can be found here: 

https://documentation.tradier.com/brokerage-api/overview/market-data

### Installing

# pip install tradier-python
Since Dan has made changes to the api, you need to install this package manually from this directory using:
`pip install .`

### Exmple

```
import os

from tradier_python import TradierAPI

token = os.environ["TRADIER_TOKEN"]
account_id = os.environ["TRADIER_ACCOUNT_ID"]
t = TradierAPI(token=token, default_account_id=account_id)

profile = t.get_profile()
print(profile)
```


## Version History

* 0.1.4
    * 
* 0.1.3
    * Include tags by default when getting orders
* 0.1.2
    * Export models from the package
* 0.1.1
    * Bug fixes
* 0.1.0
    * Initial release

## License

This project is licensed under the MIT License - see the LICENSE.md file for details

