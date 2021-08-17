---
title: 影片。游標
description: Cursor 屬性指定或抓取滑鼠停留在影片的可點按區域時，所使用的資料指標值。
ms.assetid: 2faaf9cd-47be-47d5-ad4e-8f3bb322d812
keywords:
- VIDEO. cursor Windows Media Player
topic_type:
- apiref
api_name:
- VIDEO.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73c39b40412a02e145b8063f473272184e1d7cf03caaa170de19bde7fad37a50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134241"
---
# <a name="videocursor"></a>影片。游標

**Cursor** 屬性指定或抓取滑鼠停留在影片的可點按區域時，所使用的資料指標值。

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **字串**。



| 值            | 描述                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| 系統           | 平臺相依游標 (通常是箭號) 。                                               |
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

基於轉譯目的，系統是預設的資料指標。 從此屬性抓取的預設值為 "" (空白字串) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**影片元素**](video-element.md)
</dt> </dl>

 

 





