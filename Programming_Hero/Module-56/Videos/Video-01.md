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

> END

## Navigation

⬅️ [Video-10](./Video-10.md)
➡️ [Video-02](./Video-02.md)
