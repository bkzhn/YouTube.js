[youtubei.js](../../../README.md) / [Parser](../README.md) / parse

# Function: parse()

## parse(data, requireArray, validTypes)

> **parse**\<`T`, `K`\>(`data`, `requireArray`, `validTypes`?): [`ObservedArray`](../../Helpers/type-aliases/ObservedArray.md)\<`InstanceType`\<`K`\[`number`\]\>\> \| `null`

Parses an item or an array of items.

### Type Parameters

• **T** *extends* [`YTNode`](../../Helpers/classes/YTNode.md)

• **K** *extends* [`YTNodeConstructor`](../../Helpers/interfaces/YTNodeConstructor.md)\<`T`\>[]

### Parameters

• **data**: [`RawData`](../../APIResponseTypes/type-aliases/RawData.md)

The data to parse.

• **requireArray**: `true`

Whether the data should be parsed as an array.

• **validTypes?**: `K`

YTNode types that are allowed to be parsed.

### Returns

[`ObservedArray`](../../Helpers/type-aliases/ObservedArray.md)\<`InstanceType`\<`K`\[`number`\]\>\> \| `null`

### Defined in

[src/parser/parser.ts:627](https://github.com/LuanRT/YouTube.js/blob/4ae0cc5c523a2080e68d6c0c1437c78fe318ea30/src/parser/parser.ts#L627)

## parse(data, requireArray, validTypes)

> **parse**\<`T`, `K`\>(`data`, `requireArray`, `validTypes`?): [`ObservedArray`](../../Helpers/type-aliases/ObservedArray.md)\<`InstanceType`\<`K`\>\> \| `null`

### Type Parameters

• **T** *extends* [`YTNode`](../../Helpers/classes/YTNode.md)

• **K** *extends* [`YTNodeConstructor`](../../Helpers/interfaces/YTNodeConstructor.md)\<`T`\>

### Parameters

• **data**: [`RawData`](../../APIResponseTypes/type-aliases/RawData.md)

• **requireArray**: `true`

• **validTypes?**: `K`

### Returns

[`ObservedArray`](../../Helpers/type-aliases/ObservedArray.md)\<`InstanceType`\<`K`\>\> \| `null`

### Defined in

[src/parser/parser.ts:628](https://github.com/LuanRT/YouTube.js/blob/4ae0cc5c523a2080e68d6c0c1437c78fe318ea30/src/parser/parser.ts#L628)

## parse(data, requireArray, validTypes)

> **parse**\<`T`\>(`data`?, `requireArray`?, `validTypes`?): [`SuperParsedResult`](../../Helpers/classes/SuperParsedResult.md)\<`T`\>

### Type Parameters

• **T** *extends* [`YTNode`](../../Helpers/classes/YTNode.md) = [`YTNode`](../../Helpers/classes/YTNode.md)

### Parameters

• **data?**: [`RawData`](../../APIResponseTypes/type-aliases/RawData.md)

• **requireArray?**: `false`

• **validTypes?**: [`YTNodeConstructor`](../../Helpers/interfaces/YTNodeConstructor.md)\<`T`\> \| [`YTNodeConstructor`](../../Helpers/interfaces/YTNodeConstructor.md)\<`T`\>[]

### Returns

[`SuperParsedResult`](../../Helpers/classes/SuperParsedResult.md)\<`T`\>

### Defined in

[src/parser/parser.ts:629](https://github.com/LuanRT/YouTube.js/blob/4ae0cc5c523a2080e68d6c0c1437c78fe318ea30/src/parser/parser.ts#L629)
