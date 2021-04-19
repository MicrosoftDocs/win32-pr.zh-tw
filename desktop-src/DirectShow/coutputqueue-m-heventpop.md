---
description: 當物件從佇列中移除範例時，所發出的選擇性事件。 值最初是 Null。 呼叫 COutputQueue：： SetPopEvent 方法以指定事件處理常式。
ms.assetid: f2602532-b045-4384-b87c-b28cc34c81b0
title: 'COutputQueue：： m_hEventPop 成員 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hEventPop
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 88ab5235a3d4df5b60b53279c444ae99b12fe0c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987089"
---
# <a name="coutputqueuem_heventpop-member"></a>COutputQueue：： m \_ hEventPop 成員

當物件從佇列中移除範例時，所發出的選擇性事件。 值最初是 **Null**。 呼叫 [**COutputQueue：： SetPopEvent**](coutputqueue-setpopevent.md) 方法以指定事件處理常式。

## <a name="syntax"></a>Syntax


```C++
HANDLE m_hEventPop;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Outputq (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COutputQueue 類別**](coutputqueue.md)
</dt> </dl>

 

 




