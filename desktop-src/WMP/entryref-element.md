---
title: ENTRYREF 元素
description: ENTRYREF 元素指向外部中繼檔中的專案專案。
ms.assetid: ba39db39-fa90-455b-b278-ca866ce0b69c
keywords:
- ENTRYREF 元素 Windows Media Player
topic_type:
- apiref
api_name:
- ENTRYREF Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 520a4262baf17badb136b55e7b2e216bf89d7edf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997636"
---
# <a name="entryref-element"></a>ENTRYREF 元素

**ENTRYREF** 元素指向外部中繼檔中的 **專案專案**。

``` syntax
<ENTRYREF
   HREF = "URL"
/>
```

## <a name="attributes"></a>屬性

需要) **HREF** (

參考之中繼檔的 URL。

**CLIENTBIND**

已不再支援這個屬性。

## <a name="parentchild-elements"></a>父/子項目



| 階層       | 元素                       |
|-----------------|--------------------------------|
| 父元素 | **ASX**、 **事件**、 **重複** |
| 子元素  | 無                           |



 

## <a name="remarks"></a>備註

這個元素指向外部中繼檔的內容。 Windows Media Player 處理參考之中繼檔的 **專案專案** ，就如同它們是包含在 **ENTRYREF** 元素位置的主要中繼檔中一樣。 但是，它會略過參考的中繼檔中，將 **SKIPIFREF** 屬性設定為 YES 的任何 **專案專案**。

適用于 Windows XP 的 Windows Media Player 7.0、7.1 和 Windows Media Player 會忽略參考的中繼檔中的任何 **ENTRYREF** 元素。 因此，在使用這些版本的播放程式時，中繼檔只能以一層級進行深度嵌套。 Windows Media Player 也會忽略參考檔案中的 **ASX** 元素及其屬性。 Windows Media Player 9 系列或更新版本支援嵌套最多五個層級的中繼檔。

**HREF** 屬性中指定的 url 會成為外部中繼檔中任何相對 url 的基底 url。 當外部中繼檔的專案現正播放，且使用者將它新增至程式庫時，會使用此 URL。

## <a name="examples"></a>範例


```XML
<ASX VERSION="3.0">
   <TITLE>Example of Using EntryRef</TITLE>
   <ENTRYREF HREF="https://sample.microsoft.com/metafile.asx" />
</ASX>

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------|
| 版本<br/> | Windows Media Player 70 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Windows Media 中繼檔元素參考**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Media 中繼檔參考**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





