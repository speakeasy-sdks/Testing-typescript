# pet

## Overview

Everything about your Pets

Find out more
<http://swagger.io>
### Available Operations

* [addPetForm](#addpetform) - Add a new pet to the store
* [addPetJson](#addpetjson) - Add a new pet to the store
* [addPetRaw](#addpetraw) - Add a new pet to the store
* [deletePet](#deletepet) - Deletes a pet
* [findPetsByStatus](#findpetsbystatus) - Finds Pets by status
* [findPetsByTags](#findpetsbytags) - Finds Pets by tags
* [getPetById](#getpetbyid) - Find pet by ID
* [updatePetWithForm](#updatepetwithform) - Updates a pet in the store with form data
* [updatePetForm](#updatepetform) - Update an existing pet
* [updatePetJson](#updatepetjson) - Update an existing pet
* [updatePetRaw](#updatepetraw) - Update an existing pet
* [uploadFile](#uploadfile) - uploads an image

## addPetForm

Add a new pet to the store

### Example Usage

```typescript
import { Petstore } from "petstore";
import { AddPetFormResponse } from "petstore/dist/sdk/models/operations";
import { PetStatus } from "petstore/dist/sdk/models/shared";

const sdk = new Petstore();

sdk.pet.addPetForm({
  category: {
    id: 1,
    name: "Dogs",
  },
  id: 10,
  name: "doggie",
  photoUrls: [
    "ipsam",
  ],
  status: PetStatus.Sold,
  tags: [
    {
      id: 778157,
      name: "Teri Strosin",
    },
    {
      id: 799159,
      name: "Erik Lebsack",
    },
    {
      id: 118274,
      name: "Luke McCullough",
    },
    {
      id: 944669,
      name: "Everett Breitenberg",
    },
  ],
}, {
  petstoreAuth: "",
}).then((res: AddPetFormResponse) => {
  if (res.statusCode == 200) {
    // handle response
  }
});
```

## addPetJson

Add a new pet to the store

### Example Usage

```typescript
import { Petstore } from "petstore";
import { AddPetJsonResponse } from "petstore/dist/sdk/models/operations";
import { PetStatus } from "petstore/dist/sdk/models/shared";

const sdk = new Petstore();

sdk.pet.addPetJson({
  category: {
    id: 1,
    name: "Dogs",
  },
  id: 10,
  name: "doggie",
  photoUrls: [
    "qui",
    "impedit",
  ],
  status: PetStatus.Sold,
  tags: [
    {
      id: 216550,
      name: "Brandon Auer",
    },
    {
      id: 149675,
      name: "Curtis Morissette",
    },
  ],
}, {
  petstoreAuth: "",
}).then((res: AddPetJsonResponse) => {
  if (res.statusCode == 200) {
    // handle response
  }
});
```

## addPetRaw

Add a new pet to the store

### Example Usage

```typescript
import { Petstore } from "petstore";
import { AddPetRawResponse } from "petstore/dist/sdk/models/operations";
import { PetStatus } from "petstore/dist/sdk/models/shared";

const sdk = new Petstore();

sdk.pet.addPetRaw("saepe".encode(), {
  petstoreAuth: "",
}).then((res: AddPetRawResponse) => {
  if (res.statusCode == 200) {
    // handle response
  }
});
```

## deletePet

Deletes a pet

### Example Usage

```typescript
import { Petstore } from "petstore";
import { DeletePetResponse } from "petstore/dist/sdk/models/operations";

const sdk = new Petstore();

sdk.pet.deletePet({
  apiKey: "fuga",
  petId: 449950,
}, {
  petstoreAuth: "",
}).then((res: DeletePetResponse) => {
  if (res.statusCode == 200) {
    // handle response
  }
});
```

## findPetsByStatus

Multiple status values can be provided with comma separated strings

### Example Usage

```typescript
import { Petstore } from "petstore";
import { FindPetsByStatusResponse, FindPetsByStatusStatus } from "petstore/dist/sdk/models/operations";
import { PetStatus } from "petstore/dist/sdk/models/shared";

const sdk = new Petstore();

sdk.pet.findPetsByStatus({
  status: FindPetsByStatusStatus.Pending,
}, {
  petstoreAuth: "",
}).then((res: FindPetsByStatusResponse) => {
  if (res.statusCode == 200) {
    // handle response
  }
});
```

## findPetsByTags

Multiple tags can be provided with comma separated strings. Use tag1, tag2, tag3 for testing.

### Example Usage

```typescript
import { Petstore } from "petstore";
import { FindPetsByTagsResponse } from "petstore/dist/sdk/models/operations";
import { PetStatus } from "petstore/dist/sdk/models/shared";

const sdk = new Petstore();

sdk.pet.findPetsByTags({
  tags: [
    "iure",
    "saepe",
    "quidem",
  ],
}, {
  petstoreAuth: "",
}).then((res: FindPetsByTagsResponse) => {
  if (res.statusCode == 200) {
    // handle response
  }
});
```

## getPetById

Returns a single pet

### Example Usage

```typescript
import { Petstore } from "petstore";
import { GetPetByIdResponse } from "petstore/dist/sdk/models/operations";
import { PetStatus } from "petstore/dist/sdk/models/shared";

const sdk = new Petstore();

sdk.pet.getPetById({
  petId: 99280,
}, {
  apiKey: "",
}).then((res: GetPetByIdResponse) => {
  if (res.statusCode == 200) {
    // handle response
  }
});
```

## updatePetWithForm

Updates a pet in the store with form data

### Example Usage

```typescript
import { Petstore } from "petstore";
import { UpdatePetWithFormResponse } from "petstore/dist/sdk/models/operations";

const sdk = new Petstore();

sdk.pet.updatePetWithForm({
  name: "Lela Orn",
  petId: 170909,
  status: "dolorem",
}, {
  petstoreAuth: "",
}).then((res: UpdatePetWithFormResponse) => {
  if (res.statusCode == 200) {
    // handle response
  }
});
```

## updatePetForm

Update an existing pet by Id

### Example Usage

```typescript
import { Petstore } from "petstore";
import { UpdatePetFormResponse } from "petstore/dist/sdk/models/operations";
import { PetStatus } from "petstore/dist/sdk/models/shared";

const sdk = new Petstore();

sdk.pet.updatePetForm({
  category: {
    id: 1,
    name: "Dogs",
  },
  id: 10,
  name: "doggie",
  photoUrls: [
    "explicabo",
    "nobis",
  ],
  status: PetStatus.Available,
  tags: [
    {
      id: 363711,
      name: "Velma Batz",
    },
    {
      id: 988374,
      name: "Juan O'Hara",
    },
    {
      id: 161309,
      name: "Shaun McCullough",
    },
  ],
}, {
  petstoreAuth: "",
}).then((res: UpdatePetFormResponse) => {
  if (res.statusCode == 200) {
    // handle response
  }
});
```

## updatePetJson

Update an existing pet by Id

### Example Usage

```typescript
import { Petstore } from "petstore";
import { UpdatePetJsonResponse } from "petstore/dist/sdk/models/operations";
import { PetStatus } from "petstore/dist/sdk/models/shared";

const sdk = new Petstore();

sdk.pet.updatePetJson({
  category: {
    id: 1,
    name: "Dogs",
  },
  id: 10,
  name: "doggie",
  photoUrls: [
    "molestiae",
    "velit",
  ],
  status: PetStatus.Pending,
  tags: [
    {
      id: 338007,
      name: "Kayla O'Kon",
    },
  ],
}, {
  petstoreAuth: "",
}).then((res: UpdatePetJsonResponse) => {
  if (res.statusCode == 200) {
    // handle response
  }
});
```

## updatePetRaw

Update an existing pet by Id

### Example Usage

```typescript
import { Petstore } from "petstore";
import { UpdatePetRawResponse } from "petstore/dist/sdk/models/operations";
import { PetStatus } from "petstore/dist/sdk/models/shared";

const sdk = new Petstore();

sdk.pet.updatePetRaw("quo".encode(), {
  petstoreAuth: "",
}).then((res: UpdatePetRawResponse) => {
  if (res.statusCode == 200) {
    // handle response
  }
});
```

## uploadFile

uploads an image

### Example Usage

```typescript
import { Petstore } from "petstore";
import { UploadFileResponse } from "petstore/dist/sdk/models/operations";

const sdk = new Petstore();

sdk.pet.uploadFile({
  requestBody: "sequi".encode(),
  additionalMetadata: "tenetur",
  petId: 368725,
}, {
  petstoreAuth: "",
}).then((res: UploadFileResponse) => {
  if (res.statusCode == 200) {
    // handle response
  }
});
```
