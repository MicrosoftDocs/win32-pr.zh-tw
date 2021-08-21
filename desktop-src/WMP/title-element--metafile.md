---
title: '中繼檔 (TITLE 元素) '
description: TITLE 元素會定義文字字串，以指定 ASX 或 ENTRY 專案的標題。
ms.assetid: d7ad7f00-fcf2-456d-a106-98bf0a258b81
keywords:
- " (中繼檔的 TITLE 元素) Windows Media Player"
topic_type:
- apiref
api_name:
- TITLE Element (metafile)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 085bec9a9937c8dbd02fad6df785f4bce7afea90a74117e745f09cb5135633d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117718"
---
# <a name="title-element-metafile"></a>中繼檔 (TITLE 元素) 

**TITLE** 元素會定義文字字串，以指定 **ASX** 或 **ENTRY 專案** 的標題。

``` syntax
<TITLE>
   text string
</TITLE>
```

## <a name="attributes"></a>屬性

這個元素沒有屬性。

## <a name="parentchild-elements"></a>父/子項目



| 階層       | 元素           |
|-----------------|--------------------|
| 父元素 | **ASX**， **進入** |
| 子元素  | 無               |



 

## <a name="remarks"></a>備註

這個元素會定義文字字串，以指定 **ASX** 或 **ENTRY 專案** 的標題。 標題會顯示在 [顯示面板] 和 [ **屬性** ] 對話方塊中。

當這個元素出現在 **ASX** 元素內時，文字會顯示為 [ **顯示** 資訊]。 當這個專案出現在 **ENTRY 專案** 中時，文字會顯示為 **剪輯** 資訊。

如果 **MOREINFO** 專案也與相關聯的 (父) 元素一起使用，則它是使用者按一下以存取 **MOREINFO** 專案中定義之 URL 的標題文字。

每個父 **ASX** 和 **ENTRY** 元素最多隻能包含一個子 **標題** 元素。 第一個專案之後的多個 **TITLE** 元素將會被忽略，而且不會顯示。

## <a name="examples"></a>範例


```XML
<ASX VERSION="3.0">
   <TITLE>Title of the Show</TITLE>
   <ENTRY>
      <TITLE>Title of the Clip</TITLE>
      <REF HREF="mms://example.microsoft.com/clip1.asf" />
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

 

 





