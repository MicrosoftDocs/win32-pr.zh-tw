---
title: STARTMARKER 元素
description: STARTMARKER 元素會指定 Windows Media Player 將開始呈現資料流程的標記。
ms.assetid: b5c2422b-a59c-43f7-bac3-5722418192dc
keywords:
- STARTMARKER 元素 Windows Media Player
topic_type:
- apiref
api_name:
- STARTMARKER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c3b3afbc3ab4a922d17f6a0269ed89c22f4dfeb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995443"
---
# <a name="startmarker-element"></a>STARTMARKER 元素

**STARTMARKER** 元素會指定 Windows Media Player 將開始呈現資料流程的標記。

``` syntax
<STARTMARKER
   NUMBER = "marker number"
   NAME = "marker name"
/>
```

## <a name="attributes"></a>屬性

**數量**

索引中數值標記的數目。 預設值是即時資料流中的隨選內容或目前位置的開始位置。

**名稱**

索引中命名標記的名稱。 預設值是即時資料流中的隨選內容或目前位置的開始位置。

## <a name="parentchild-elements"></a>父/子項目



| 階層       | 元素           |
|-----------------|--------------------|
| 父元素 | **ENTRY**、 **REF** |
| 子元素  | 無               |



 

## <a name="remarks"></a>備註

這個元素會指定 Windows Media Player 用來開始轉譯父 **專案** 或 **REF** 元素中定義之資料流程的標記。

**注意**

您可以使用 **數位** 或 **名稱** 屬性來使用此元素，但不能同時使用兩者。

在 **ref** 元素內定義的 **STARTMARKER** 元素優先于 **Ref** 元素的父 **專案專案** 中所定義的 **STARTMARKER** 元素。 **STARTMARKER** 元素也優先于 **STARTTIME** 元素。

如果 **STARTMARKER** 元素所指定的標記在資料流程中的後面比 **ENDMARKER** 專案所定義的標記還新，則不會播放任何內容，但不會產生任何錯誤。

## <a name="examples"></a>範例


```XML
<STARTMARKER NUMBER="14" />
<STARTMARKER NAME="Marker_StartHere" />
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

 

 





