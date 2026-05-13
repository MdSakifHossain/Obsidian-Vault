# 56-1 Project Setup, Load Data from API

⬅️ [Module 56](../Module-56.md)

> START

- [ ] implement the private route
- [ ] making a custom gradient button using ChatGPT.
- [ ] Homepage logic: we will need `Recent Products` so, we need to make an `API Endpoint` for that.
- [ ] Backend: create a `GET /latest-products` endpoint.

```js
app.get("/latest-products", async (req, res) => {
  const result = productCollection
    .find({})
    .sort({ created_at: -1 })
    .limit(6)
    .toArry();

  res.json(result);
});
```

- [ ] Create the `latestProductsPromise` and pass it into the `LatestProducts` Component

```jsx
import React from "react";

// 1. create the latest products promise
const latestProductsPromise = fetch(
  "http://localhost:3000/latest-products",
).then((res) => res.json());

const Homepage = () => {
  return (
    <div>
      <h2>This is HomePage</h2>

      {/* 2. add the promise into this component */}
      <LatestProducts
        latestProductsPromise={latestProductsPromise}
      ></LatestProducts>
    </div>
  );
};

export default Homepage;
```

- [ ] Create the `LatestProducts` Compoent and then:

```jsx
import React from "react";

// 1. Destructure the promise
const LatestProducts = ({ latestProductsPromise }) => {
  // 2. do the react magic to resolve the promise
  const products = use(latestProductsPromise);
  // 3. check if products are there or not
  console.log(products);

  return (
    <div>
      <p>Latest Products</p>
    </div>
  );
};

export default LatestProducts;
```

> END

## Navigation

⬅️ [Video-10](./Video-10.md)
➡️ [Video-02](./Video-02.md)
