# store

## Overview

Access to Petstore orders

Find out more about our store
<http://swagger.io>
### Available Operations

* [deleteOrder](#deleteorder) - Delete purchase order by ID
* [getInventory](#getinventory) - Returns pet inventories by status
* [getOrderById](#getorderbyid) - Find purchase order by ID
* [placeOrderForm](#placeorderform) - Place an order for a pet
* [placeOrderJson](#placeorderjson) - Place an order for a pet
* [placeOrderRaw](#placeorderraw) - Place an order for a pet

## deleteOrder

For valid response try integer IDs with value < 1000. Anything above 1000 or nonintegers will generate API errors

### Example Usage

```typescript
import { Petstore } from "petstore";
import { DeleteOrderResponse } from "petstore/dist/sdk/models/operations";

const sdk = new Petstore();

sdk.store.deleteOrder({
  orderId: 662527,
}).then((res: DeleteOrderResponse) => {
  if (res.statusCode == 200) {
    // handle response
  }
});
```

## getInventory

Returns a map of status codes to quantities

### Example Usage

```typescript
import { Petstore } from "petstore";
import { GetInventoryResponse } from "petstore/dist/sdk/models/operations";

const sdk = new Petstore();

sdk.store.getInventory({
  apiKey: "YOUR_API_KEY_HERE",
}).then((res: GetInventoryResponse) => {
  if (res.statusCode == 200) {
    // handle response
  }
});
```

## getOrderById

For valid response try integer IDs with value <= 5 or > 10. Other values will generate exceptions.

### Example Usage

```typescript
import { Petstore } from "petstore";
import { GetOrderByIdResponse } from "petstore/dist/sdk/models/operations";
import { OrderStatus } from "petstore/dist/sdk/models/shared";

const sdk = new Petstore();

sdk.store.getOrderById({
  orderId: 820994,
}).then((res: GetOrderByIdResponse) => {
  if (res.statusCode == 200) {
    // handle response
  }
});
```

## placeOrderForm

Place a new order in the store

### Example Usage

```typescript
import { Petstore } from "petstore";
import { PlaceOrderFormResponse } from "petstore/dist/sdk/models/operations";
import { OrderStatus } from "petstore/dist/sdk/models/shared";

const sdk = new Petstore();

sdk.store.placeOrderForm({
  complete: false,
  id: 10,
  petId: 198772,
  quantity: 7,
  shipDate: new Date("2022-11-26T13:23:33.410Z"),
  status: OrderStatus.Approved,
}).then((res: PlaceOrderFormResponse) => {
  if (res.statusCode == 200) {
    // handle response
  }
});
```

## placeOrderJson

Place a new order in the store

### Example Usage

```typescript
import { Petstore } from "petstore";
import { PlaceOrderJsonResponse } from "petstore/dist/sdk/models/operations";
import { OrderStatus } from "petstore/dist/sdk/models/shared";

const sdk = new Petstore();

sdk.store.placeOrderJson({
  complete: false,
  id: 10,
  petId: 198772,
  quantity: 7,
  shipDate: new Date("2021-04-29T07:12:18.684Z"),
  status: OrderStatus.Approved,
}).then((res: PlaceOrderJsonResponse) => {
  if (res.statusCode == 200) {
    // handle response
  }
});
```

## placeOrderRaw

Place a new order in the store

### Example Usage

```typescript
import { Petstore } from "petstore";
import { PlaceOrderRawResponse } from "petstore/dist/sdk/models/operations";
import { OrderStatus } from "petstore/dist/sdk/models/shared";

const sdk = new Petstore();

sdk.store.placeOrderRaw("laborum".encode()).then((res: PlaceOrderRawResponse) => {
  if (res.statusCode == 200) {
    // handle response
  }
});
```
