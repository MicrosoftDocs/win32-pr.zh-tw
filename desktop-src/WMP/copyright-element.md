---
title: '著作權元素 (Msfeeds .h) '
description: 著作權元素會定義文字字串，以指定 ASX 或 ENTRY 元素的著作權資訊。
ms.assetid: 264b92de-b10c-41b9-b219-727879079f15
keywords:
- 著作權元素 Windows Media Player
topic_type:
- apiref
api_name:
- COPYRIGHT Element
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83b757528cfb14a01854346854a342ee9faced65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980113"
---
# <a name="copyright-element"></a>著作權元素

**著作權** 元素會定義文字字串，以指定 **ASX** 或 **ENTRY** 元素的著作權資訊。

``` syntax
<COPYRIGHT>
    text string
</COPYRIGHT>
```

## <a name="attributes"></a>屬性

這個元素沒有屬性。

## <a name="parentchild-elements"></a>父/子項目



| 階層       | 元素           |
|-----------------|--------------------|
| 父元素 | **ASX**， **進入** |
| 子元素  | 無               |



 

## <a name="remarks"></a>備註

此元素會定義文字字串，以指定 **ASX** 或 **ENTRY 專案** 的著作權資訊。

當此元素出現在 **ASX** 元素內時，著作權字串只會顯示為 [ **顯示** 資訊]。 當這個專案出現在 **ENTRY 專案** 中時，文字會顯示為剪輯資訊。 每個父 **ASX** 和 **ENTRY** 元素最多隻能包含一個子 **著作權** 元素。 第一個的多個 **著作權** 元素會被忽略，且不會顯示。

如果未使用 UTF-8 編碼配置來編碼中繼檔，則著作權和商標注冊符號 ( 或 ) 的字元可能無法正確顯示。 在此情況下，若要為所有使用者正確顯示這些符號的其中一個，您可以改用 ASCII 對等專案 (c) 和 (R) 。

如果中繼檔是使用 UTF-8 編碼，則著作權和商標符號將會正確顯示。

## <a name="examples"></a>範例


```XML
<COPYRIGHT>Copyright (c) 1998, Microsoft Corporation</COPYRIGHT>

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/>                                 |
| 標頭<br/>  | <dl> <dt>Msfeeds。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**將著作權字元新增至中繼檔**](adding-copyright-characters-to-metafiles.md)
</dt> <dt>

[**Windows Media 中繼檔元素參考**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Media 中繼檔參考**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





