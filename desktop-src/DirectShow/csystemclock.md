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
ms.openlocfilehash: e9cc5e0bde8983cfd8c544d3898d4af628e10f87
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104568033"
---
# <a name="csystemclock-class"></a>CSystemClock 類別

![csystemclock 類別階層](images/sclock01.png)

`CSystemClock`類別會執行傳回系統時間的時鐘。

這個類別衍生自 [**CBaseReferenceClock**](cbasereferenceclock.md) 類別，並新增 **IPersist** 和 [**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust) 介面的支援。



| 公用方法                                        | Description                                         |
|-------------------------------------------------------|-----------------------------------------------------|
| [**CreateInstance**](csystemclock-createinstance.md) | 建立這個物件的新執行個體。              |
| [**CSystemClock**](csystemclock-csystemclock.md)     | 函式方法。                                 |
| IAMClockAdjust 方法                                | Description                                         |
| [**SetClockDelta**](csystemclock-setclockdelta.md)   | 調整時鐘時間。                             |
| IPersist 方法                                      | Description                                         |
| [**GetClassID**](csystemclock-getclassid.md)         | 傳回物件 (CLSID) 的類別識別碼。 |



 

 

 



