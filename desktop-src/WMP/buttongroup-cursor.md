---
title: BUTTONGROUP 資料指標
description: Cursor 屬性指定或抓取當滑鼠停留在 BUTTONGROUP 的按鈕上時，所顯示的游標類型。
ms.assetid: c1b7e3e1-862b-48c1-bd2d-d9abd9ada14c
keywords:
- BUTTONGROUP. cursor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b3de12950aed383f48dcde5d8978724037f86e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977565"
---
# <a name="buttongroupcursor"></a>BUTTONGROUP 資料指標

**Cursor** 屬性指定或抓取當滑鼠停留在 **BUTTONGROUP** 的按鈕上時，所顯示的游標類型。

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>可能的值

這個屬性是包含下列其中一個值的讀取/寫入 **字串** 。



| 值            | 描述                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| 系統           | 預設值。 平臺相依游標 (通常是箭號) 。                                      |
| 手             | 手。                                                                                       |
| help             | 有問號的箭號可用來指出說明。                                      |
| sizeall          | 四指向的箭號，指向北、南、東和西。                                   |
| sizenesw         | 指向東北和西南的雙指向箭號。                                      |
| sizens           | 指向北和南的雙指向箭號。                                              |
| sizenwse         | 雙指向箭號，指向西北和東南部。                                      |
| sizewe           | 指向 west 和東的雙指向箭號。                                                |
| uparrow          | 垂直箭號向上。                                                             |
| \*ani 或 \* 中 | 任何 ani 或..................................)  ( |



 

## <a name="remarks"></a>備註

指定的資料指標會套用至 **BUTTONGROUP** 中的所有按鈕。

如果您指定不正確資料指標值，它會維持在先前設定的值。

資料指標檔名稱路徑會被忽略，因此游標檔必須位於預設目錄中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BUTTONGROUP 元素**](buttongroup-element.md)
</dt> </dl>

 

 





