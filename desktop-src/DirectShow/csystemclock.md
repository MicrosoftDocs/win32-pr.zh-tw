---
description: CSystemClock 類別會執行傳回系統時間的時鐘。
ms.assetid: 22f8b641-6472-433f-bff4-4e62eae25c9b
title: CSystemClock 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock
api_type:
- COM
api_location: ''
ms.openlocfilehash: c608b1d3f44a82d7aa964e803dec147a7216a71e85c6d797135713cf28af3fa0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317220"
---
# <a name="csystemclock-class"></a>CSystemClock 類別

![csystemclock 類別階層](images/sclock01.png)

`CSystemClock`類別會執行傳回系統時間的時鐘。

這個類別衍生自 [**CBaseReferenceClock**](cbasereferenceclock.md) 類別，並新增 **IPersist** 和 [**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust) 介面的支援。



| 公用方法                                        | 描述                                         |
|-------------------------------------------------------|-----------------------------------------------------|
| [**CreateInstance**](csystemclock-createinstance.md) | 建立這個物件的新執行個體。              |
| [**CSystemClock**](csystemclock-csystemclock.md)     | 函式方法。                                 |
| IAMClockAdjust 方法                                | 描述                                         |
| [**SetClockDelta**](csystemclock-setclockdelta.md)   | 調整時鐘時間。                             |
| IPersist 方法                                      | 描述                                         |
| [**GetClassID**](csystemclock-getclassid.md)         | 傳回物件 (CLSID) 的類別識別碼。 |



 

 

 



