# Public Index Specification

This is a very simple way of maintaining menu data, now what we are already publicly storing the menu photos here in this repository. It saves many, many steps in repeatedly moving around data from system to system, and/or within each system.

## Current Indices:

* **Brands**: https://github.com/LeftCoastCollective/menu/blob/master/brands.xml
* **Items**: https://github.com/LeftCoastCollective/menu/blob/master/items.xml

---

The `Left Coast` menu spreads across regions, with one index of many items shared between all the areas. For that reason, `Product` information that matters to humans is stored apart from the inventory records themselves, in a system many can manage ( with supervision and quality control ) versus giving everyone access to a "light" form of asset management just to maintain the attributes and public-facing content associated with an `Item` offered online.

Inventory systems contain so-called "sensitive" information, but that only really involves `Cost` vs. `Price`, `Stock Adjustments`, `Stock Levels`, `Stock Locations`, `Movement History`, and `Transactions`, etc. That is the difference between an `Item` and a `Product`. The `Product` is an abstract _idea_ used by computers and insiders who understand inventory management. `Items` are descriptions of objects we buy, usually consume, and all which have "real" information we actually care about. `Items` are _things_ anyone ought to be able to understand, find out more about, and ultimately obtain.

## Items

- Are referenced by a `SKU` that is unique to them, but which gives clues to its `Brand` if any.

The `Item` data is real-world information people need, such as:
- `Brand` code(s) that identify who cultivates, manufactures, or otherwise produces the product.
- A full-text/markdown `Description` that can be changed in once place then automatically changes everywhere it exists.
- `Media` attachments such as photos and videos, with full meta data potentially added; such as resolution, format, etc.
- `Tags` ( new, necessary for better highlighting of celebrity/veteran choices easily by hashtagging )
- `Category` Codes ( previously one category only )
- `Varieties`, a list of other `SKU` codes that exist for the same item, but in a different form.

## Brands

- Are refererenced by a unique `ID` that is part of the `SKU` of their `Items` in the index.

And then there is the information about the producer, separate of the `Item` information:
- A display `Name` the brand refers to itself by.
- The `Instagram/IG` and/or `Twitter/Tw`, `Facebook/Fb`, `LinkedIn/Li` profiles, etc.
- `Logo` for the brand.
- `URL` for their website.
- More in the future, such as a promotional materials, etc.

All this information comes together in every `Product Description` for purchasing online, but it need not be entered in many different places. Instead we keep it here in this index which all regions maintain. It is intentionally "almost" human readable and not overly intimidating to look at and pretty easily figure out what it means.

## Template Segments

#### These are what typical `Item` segments would look like in the `items.xml` index:

```xml
<Item SKU="TEG-BISCOTTI-3G5">
  <Brand>TEG</Brand>
  <Description>...</Description>
  <Media>
    <Image height="..." width="...">URL0</Image>
    <Image>URL1</Image>
    <Video>URL2</Video>
  </Media>
  <Tags>...</Tags>
  <Categories>...</Categories>
</Item>
<Item SKU='STICKY-SLH'>
  <Brand>STICKY</Brand>
  <Description>...</Description>
  <Media>
    <Image>URL0</Image>
  </Media>
  <Tags>...</Tags>
  <Categories>...</Categories>
  <Varieties>
    <Variety SKU="STICKY-SLH-4G">Eighth</Variety>
    <Variety SKU="STICKY-SLH-8G">Quarter</Variety>
    <Variety SKU="STICKY-SLH-HO">Half Ounce</Variety>
    <Variety SKU="STICKY-SLH-OZ">Ounce</Variety>
  </Varieties>
</Item>
```

#### This is what typical `Brand` segments would look like in the `brands.xml` index:

```xml
<Brand ID="TEG">
  <Name>Team Elite Genetics</Name>
  <Logo>...</Logo>
  <URL>...</URL>
  <IG>teamelitegenetics</IG>
</Brand>
<Brand ID="STICKY">
  <Name>Sticky Farms</Name>
  <IG>sticky_farms</IG>
</Brand>
```

---

This index is not intended to be directly edited manually, except in extreme or early circumstances. The idea is to manage this information in a separate database, but toexport to this format which can be easily and publicly shared.

## To be added to the index:

- [ ] Allow inclusion of other files by link, such as all the items of a certain brand together.
- [ ] Allow inclusion of other item or brand data specifically, such as items sharing the same description.
