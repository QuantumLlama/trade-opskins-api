# API Documentation for [WAX ExpressTrade](https://trade.opskins.com)

### **🚨 Breaking Change Notice 🚨**
- `items` input on `ITrade/SendOffer` & `ITrade/SendOfferToSteamId` endpoints will be **completely disabled on *October 22nd, 2018***. Please switch to using these two inputs instead: `items_to_send` & `items_to_receive`. Thank you for your cooperation and understanding.

## API Interfaces

* [ICase](ICase.md)
* [ICaseSite](ICaseSite.md)
* [IEthereum](IEthereum.md)
* [IItem](IItem.md)
* [ITest](ITest.md)
* [ITrade](ITrade.md)
* [IUser](IUser.md)

## API Response

Direct URL to API: https://api-trade.opskins.com

All *successful* API responses have return data within the "response" object.  A typical response may look like this:

```json
{
    "status": 1,
    "time": 1528334546,
    "response": {
        "offer": {
            "some_data": "here"
        }
    }
}
```

If a response is paginated, the pagination details (`current_page` and `total_pages`) occur at the top-level of the object, not inside the `response` body.

#### Response Status Codes
All `status` codes and their titles can be found [here](https://github.com/OPSkins/trade-opskins-api/issues/19#issuecomment-403122935).

## OAuth
OPSkins OAuth works automatically with WAX ExpressTrade. You can use OAuth to log users into your website via OPSkins and (if desired) perform actions on their behalf via the API. Please see [OPSkins OAuth Docs](https://docs.opskins.com/public/en.html#oauth) for more information.

## Additional Notes
- On some endpoints you may be required to send a `twofactor_code`. Please see [this comment](https://github.com/OPSkins/trade-opskins-api/issues/16#issuecomment-399715578) if you need help.
- For transferring items from OPSkins to WAX ExpressTrade, see: [OPSkins Docs: IInventory/TransferToTradeSite/v1](https://docs.opskins.com/public/en.html#IInventory_TransferToTradeSite_v1)
