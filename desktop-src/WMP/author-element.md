---
title: AUTHOR 元素
description: author 元素包含 Windows 媒體中繼檔或媒體剪輯的作者名稱。
ms.assetid: d80aad3d-4471-4310-8d43-2733ed83103c
keywords:
- AUTHOR 元素 Windows Media Player
topic_type:
- apiref
api_name:
- AUTHOR Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 058753d73049debe01e442f49bf12476642111549ad890e931100026badaeb3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098888"
---
# <a name="author-element"></a>AUTHOR 元素

**author** 元素包含 Windows 媒體中繼檔或媒體剪輯的作者名稱。

``` syntax
<AUTHOR>   
   text string
</AUTHOR>
```

## <a name="attributes"></a>屬性

這個元素沒有屬性。

## <a name="parentchild-elements"></a>父/子項目



| 階層       | 元素            |
|-----------------|--------------------|
| 父元素 | **ASX**， **進入** |
| 子元素  | 無               |



 

## <a name="remarks"></a>備註

這個元素包含代表 Windows 媒體中繼檔或媒體剪輯之作者名稱的文字字串。 您可以使用 **ASX** 元素內的 AUTHOR 元素，以及 **專案專案** 內的 **AUTHOR** 專案。

如果此元素出現在 **ASX** 專案中，則文字會顯示為 [ **顯示** 資訊]。

如果這個元素出現在 **ENTRY 專案** 中，文字就會顯示為剪輯作者。

每個父 **ASX** 和 **ENTRY** 元素最多隻能包含一個子 **作者** 元素。 第一個專案之後的多個 **AUTHOR** 元素將會被忽略，且不會顯示。

## <a name="examples"></a>範例


```XML
<ASX VERSION="3.0">
   <AUTHOR>Neal S.</AUTHOR>   <!-- Show author -->
   <ENTRY>
      <REF HREF="mms://example.microsoft.com/clip1.asf" />
      <AUTHOR>Robert P.</AUTHOR>  <!-- Clip author -->
   </ENTRY>
</ASX>

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------|
| 版本<br/> | Windows Media Player 70 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Windows媒體中繼檔元素參考**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows媒體中繼檔參考**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





