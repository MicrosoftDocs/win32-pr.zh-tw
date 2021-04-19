---
title: BUTTONELEMENT 資料指標
description: Cursor 屬性會指定或抓取滑鼠移到 BUTTONELEMENT 上時所顯示的 BUTTONELEMENT 資料指標值。
ms.assetid: 29e7fadb-30d8-40e4-9a64-6b6f45eac80a
keywords:
- BUTTONELEMENT. cursor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f267cd54c36ad8f89a7242d7f428fd0d52b75fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979613"
---
# <a name="buttonelementcursor"></a>BUTTONELEMENT 資料指標

**Cursor** 屬性會指定或抓取滑鼠移到 **BUTTONELEMENT** 上時所顯示的 **BUTTONELEMENT** 資料指標值。

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **字串**。



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

如果指定了不正確值，則會保留先前的值。

資料指標檔名稱路徑會被忽略，因此游標檔必須位於預設目錄中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BUTTONELEMENT 元素**](buttonelement-element.md)
</dt> </dl>

 

 





