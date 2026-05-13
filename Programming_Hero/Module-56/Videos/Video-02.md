# 56-2 Design Card and show latest products

⬅️ [Module 56](../Module-56.md)

> START

- [ ] since we have the products, we can now show the `Product Cards` and move on
- [ ] Create a `Product Details` so that each products `view details` button will point to that product details page
- [ ] create a path on the router so for the `/productDetails/:id` which will point to the product details
- [ ] make sure to add the loader and fetch the data on the loader of `/productDetails/:id` then give the data to the page component.

```jsx
{
  path: "productDetails/:id",
  loader: ({ params }) => fetch(`http://localhost:3000/products/${params.id}`),
  Component: ProductDetailsPage,
}
```

- [ ] in the `Page Details Page`, we will access that data

```jsx
// ProductDetailsPage.jsx
import React from "react";

const ProductDetailsPage = () => {
  // 1. access the loader data with
  const product = useLoaderData();
  // 2. check the prodcut data
  console.log(product);

  return (
    <div>
      <h1>Product Details Page</h1>
    </div>
  );
};

export default ProductDetailsPage;
```

- [ ] clicking on the `I want to Buy this product` button on the `ProductDetails` page will trigger a dialogue which is basically a `Form`.

> END: GO to the next page

## Navigation

⬅️ [Video-01](./Video-01.md)
➡️ [Video-03](./Video-03.md)
