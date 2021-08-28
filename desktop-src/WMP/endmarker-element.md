---
title: ENDMARKER 元素
description: ENDMARKER 元素會指定 Windows Media Player 將停止轉譯資料流程的標記。
ms.assetid: 554f0612-1669-4da4-9c5f-cc8984ef897c
keywords:
- ENDMARKER 元素 Windows Media Player
topic_type:
- apiref
api_name:
- ENDMARKER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 276b17117d2f01d9bc40d7f171a6d0ff6ea2331da439266ac11bf8c25b5e4f25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996658"
---
# <a name="endmarker-element"></a>ENDMARKER 元素

**ENDMARKER** 元素會指定 Windows Media Player 將停止轉譯資料流程的標記。

``` syntax
<ENDMARKER
   NUMBER = "marker number" |
   NAME = "marker name"
/>
```

## <a name="attributes"></a>屬性

**數量**

索引中數值標記的數目。 預設值是內容的結尾。

**名稱**

索引中命名標記的名稱。 預設值是內容的結尾。

## <a name="parentchild-elements"></a>父/子項目



| 階層       | 元素           |
|-----------------|--------------------|
| 父元素 | **ENTRY**、 **REF** |
| 子元素  | 無               |



 

## <a name="remarks"></a>備註

這個元素會指定標記，其中 Windows Media Player 是用來停止轉譯在父 **專案** 或 **REF** 元素中定義的資料流程。

注意

使用具有 **NUMBER** 或 **NAME** 屬性的 **ENDMARKER** 元素，但不能同時使用兩者。

在預覽模式中，即使 **PREVIEWDURATION** 元素所指定的時間尚未經過，到達結束標記也會停止預覽。 **ENDMARKER** 元素也優先于 **DURATION** 元素。

在 **ref** 元素內定義的 **ENDMARKER** 元素優先于 **Ref** 元素的父 **專案專案** 內定義的 **ENDMARKER** 。

如果 **ENDMARKER** 元素所指定的標記在資料流程中比 **STARTMARKER** 專案所定義的標記稍早出現，則不會播放任何內容，但不會產生任何錯誤。

## <a name="examples"></a>範例


```XML
<ENDMARKER NUMBER="17" />
<ENDMARKER NAME="Marker_StopHere" />

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

 

 





