# Public Index Specification

The `Left Coast` menu spreads across many regions, but it has one registry with many items shared between areas. For that reason, `Product` information that matters to humans is stored apart from the inventory records themselves. The inventory systems only need to know things like `Stock Levels`, `Storage Locations`, `Movement History`, etc. That is the difference betwen an `Item` and a `Product`.

The `Product` is an abstract idea, used by computers and insiders trained to understand inventory management. `Items` are physical objects we buy, usually consume, and all which have "real" information we actually care about, such as:

- A `SKU` that is unique to it, but which gives clues to its `Brand` if any.
- `Brand` code(s) that identify who cultivates, manufactures, or otherwise produces the product.
- A full-text/markdown `Description` that can be changed in once place then automatically changes everywhere it exists.
- Content attachments such as photos and videos, with full meta data potentially added; such as resolution, format, etc.
- `Tags` ( new, necessary for better highlighting of celebrity/veteran choices easily by hashtagging )
- `Category` Codes ( previously one category only )

And then there is `Brand` information including:
- A unique `ID` that is part of the `SKU` for `Products`
- A display `Name` the `Brand` refers to itself by.
- The `Instagram` and/or `Twitter`, `Facebook`, `LinkedIn` profiles, etc.
- Website address.

All this information comes together in every `Product Description` for purchasing online, but it need not be entered in many different places. Instead we keep it here in this index which all regions maintain. It is intentionally "almost" human readable and not overly intimidating to look at and pretty easily figure out what it means.

## Template Segments

#### These are what typical `Item` segments would look like in the `items.xml` index:

```xml
<Item SKU="TEG-BISCOTTI-3G5">
  <Brand>TEG</Brand>
  <Description>...</Description>
  <Media>
    <Image>URL0</Image>
    <Image>URL1</Image>
    <Video>URL2</Video>
  </Media>
  <Tags>...</Tags>
  <Categories>...</Categories>
</Item>
<Item SKU='STICKY-SLH-4G0'>
  <Brand>STICKY</Brand>
  <Description>...</Description>
  <Media>
    <Image>URL0</Image>
  </Media>
  <Tags>...</Tags>
  <Categories>...</Categories>
</Item>
```

#### This is what typical `Brand` segments would look like in the `brands.xml` index:

```xml
<Brand ID="TEG">
  <Name>Team Elite Genetics</Name>
  <IG>teamelitegenetics</IG>
</Brand>
<Brand ID="STICKY">
  <Name>Sticky Farms</Name>
  <IG>sticky_farms</IG>
</Brand>
```

---

This index is not intended to be directly edited manually, except in extreme or early circumstances. The idea is to manage this information in a separate database, but toexport to this format which can be easily and publicly shared.
