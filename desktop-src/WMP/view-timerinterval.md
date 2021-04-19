---
title: TimerInterval
description: TimerInterval 屬性會指定或抓取計時器引發事件至 ontimer 事件處理常式的間隔（以毫秒為單位）。
ms.assetid: 1a69890f-5ea4-493a-8a9e-04fe60a41804
keywords:
- TimerInterval Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.timerInterval
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 790c95fbb2cded134222271d04c4c37dae412b8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992146"
---
# <a name="viewtimerinterval"></a>TimerInterval

**TimerInterval** 屬性會指定或抓取計時器引發事件至 **ontimer** 事件處理常式的間隔（以毫秒為單位）。

``` syntax
        elementID.timerInterval
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **號碼** (**長**) ，預設值為1000。



| 值        | 描述                    |
|--------------|--------------------------------|
| 0            | 計時器事件不會引發。 |
| 50 及以上 | 以毫秒為單位的間隔。  |



 

低於 50 (的任何值都包含負數，但不包括零) 會產生錯誤，並維持先前的值。

## <a name="remarks"></a>備註

如果未執行任何 **ontimer** 事件處理常式，則不會自動引發。 因此，即使預設值為非零，也不會降低效能。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**VIEW 元素**](view-element.md)
</dt> <dt>

[**VIEW. ontimer**](view-ontimer.md)
</dt> </dl>

 

 





