# Public Index Specification

The `Left Coast` menu spreads across many regions, but it has one registry with many items shared between areas. For that reason, `Product` information that matters to humans is stored apart from the inventory records themselves. The inventory systems only need to know things like `Stock Levels`, `Storage Locations`, `Movement History`, etc. That is the difference betwen an `Item` and a `Product`.

The `Product` is an abstract idea, used by computers and insiders trained to understand inventory management. `Items` are physical objects we buy, usually consume, and all which have "real" information we actually care about, such as:

- A full-text/markdown `Description` that can be changed in once place then automatically changes everywhere it exists.
- `Brand` code(s) that identify who cultivates, manufactures, or otherwise produces the product.
- Content attachments such as photos and videos, with full meta data potentially added; such as resolution, format, etc.
- `Tags` ( new, necessary for better highlighting of celebrity/veteran choices easily by hashtagging )
- `Category` Codes ( previously one category only )

And then there is `Brand` information including:
- A unique `Code` that is part of the `SKU` for `Products`
- A display `Name` the `Brand` refers to itself by.
- The `Instagram` and/or `Twitter`, `Facebook`, `LinkedIn` profiles, etc.
- Website address.

All this information comes together in every `Product Description` for purchasing online, but it need not be entered in many different places. Instead we keep it here in this index which all regions maintain.

## Template Segments

#### This is what a typical `Item` segment would look like in the `items.xml` index:

```
<XML>

</XML>
```

#### This is what a typical `Brand` segment would look like in the `brands.xml` index:

```
<XML>

</XML>
```
