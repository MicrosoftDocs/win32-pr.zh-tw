---
title: DURATION 元素
description: DURATION 元素會定義 Windows Media Player 將呈現相關聯的播放清單專案的時間長度。
ms.assetid: fe5c242e-08c9-44f0-a6fc-3f0fa432ba38
keywords:
- DURATION 元素 Windows Media Player
topic_type:
- apiref
api_name:
- DURATION Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0446fd207ce04ab08d4c7bd2e055ef8d11a5a36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994837"
---
# <a name="duration-element"></a>DURATION 元素

**DURATION** 元素會定義 Windows Media Player 將呈現相關聯的播放清單專案的時間長度。

``` syntax
<DURATION
    VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a>屬性

**值** (必要) 

Windows Media Player 呈現專案的時間長度（以小時、分鐘、秒和百分之一秒為單位）。 預設值是專案的整個長度。 如果專案是圖形檔案，則必須指定持續時間值。

## <a name="parentchild-elements"></a>父/子項目



| 階層       | 元素           |
|-----------------|--------------------|
| 父元素 | **ENTRY**、 **REF** |
| 子元素  | 無               |



 

## <a name="remarks"></a>備註

這個元素會定義要轉譯資料流程的時間長度。 如果 **VALUE** 屬性超過內容資料流程的長度，資料流程就會在其正常端點終止。

這個元素可以出現在 **REF** 元素或 **ENTRY** 元素內。 不過，在 **ref** 元素內定義的 DURATION 元素，會覆寫在 **ref** 元素的父 **專案專案** 中顯示的 **DURATION** 元素。

**DURATION** 元素會覆寫 **PREVIEWDURATION** 元素。

## <a name="examples"></a>範例


```XML
<DURATION VALUE="00:00:30" />   <!-- 30 seconds -->
<DURATION VALUE="1:01.5" />     <!-- 61.5 seconds -->

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Windows Media 中繼檔元素參考**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Media 中繼檔參考**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





