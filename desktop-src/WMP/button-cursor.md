---
title: 按鈕。游標
description: Cursor 屬性會指定或抓取滑鼠指標停留在按鈕上時所顯示的游標。
ms.assetid: 19bdbb23-00e2-45cf-b67d-9ada036b9c3b
keywords:
- Cursor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2641491a5a73498da2c43fd74d4187b5594e177
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998393"
---
# <a name="buttoncursor"></a>按鈕。游標

**Cursor** 屬性會指定或抓取滑鼠指標停留在 **按鈕** 上時所顯示的游標。

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **字串**。



| 值            | 描述                                                                                |
|------------------|--------------------------------------------------------------------------------------------|
| 系統           | 預設值。 平臺相依游標 (通常是箭號) 。                                     |
| 手             | 手。                                                                                      |
| help             | 有問號的箭號可用來指出說明。                                     |
| sizeall          | 四指向的箭號，指向北、南、東和西。                                  |
| sizenesw         | 指向東北和西南的雙指向箭號。                                     |
| sizens           | 指向北和南的雙指向箭號。                                             |
| sizenwse         | 雙指向箭號，指向西北和東南部。                                     |
| sizewe           | 指向 west 和東的雙指向箭號。                                               |
| uparrow          | 垂直箭號向上。                                                            |
| \*ani 或 \* 中 | 任何 ani 或............)  (.....................。 |



 

## <a name="remarks"></a>備註

如果系統無法辨識指定的資料指標值，則資料指標值會維持在先前設定的值。

資料指標檔名稱路徑會被忽略，因此游標檔必須位於預設目錄中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BUTTON 元素**](button-element.md)
</dt> </dl>

 

 





