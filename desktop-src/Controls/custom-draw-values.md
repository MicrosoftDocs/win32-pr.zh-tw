---
title: '自訂繪製值 (CommCtrl .h) '
description: 此區段會列出用來識別資料列控制群組件的值。
ms.assetid: 154321c7-99f8-4ed5-a5ff-fb96126b43c7
topic_type:
- apiref
api_name:
- TBCD_CHANNEL
- TBCD_THUMB
- TBCD_TICS
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccf05ab951fdc83ec5be414688be56d710ba0d98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979421"
---
# <a name="custom-draw-values"></a>自訂繪製值

此區段會列出用來識別資料列控制群組件的值。



| 常數                                                                                                                                                   | 描述                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| <span id="TBCD_CHANNEL"></span><span id="tbcd_channel"></span><dl> <dt>**TBCD \_ 通道**</dt> </dl> | 識別 [對齊程式] 控制項的 thumb 標記所投影的通道。<br/>                        |
| <span id="TBCD_THUMB"></span><span id="tbcd_thumb"></span><dl> <dt>**TBCD \_ THUMB**</dt> </dl>       | 識別 [資料指標] 控制項的 [thumb] 標記。 這是使用者移動之控制項的一部分。<br/> |
| <span id="TBCD_TICS"></span><span id="tbcd_tics"></span><dl> <dt>**TBCD \_ TICS**</dt> </dl>          | 識別顯示在 [側邊] 控制項邊緣的刻度。<br/>                      |



## <a name="remarks"></a>備註

例如，自訂繪製值是在 [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的 **dwItemSpec** 成員中指定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>CommCtrl。h</dt> </dl> |



 

 





