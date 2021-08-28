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
ms.openlocfilehash: bb401cf9755260c797ebfb382d9f2248d9d04c5f8d9e9b49e319c390de1664c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087208"
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

 

 




