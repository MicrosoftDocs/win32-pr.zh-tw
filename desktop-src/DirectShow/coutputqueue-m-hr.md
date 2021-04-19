---
description: HRESULT 值，指出物件是否會接受範例。 如果值為 S \_ OK，則物件會接受範例。 否則，它會拒絕範例。
ms.assetid: e05d4d2e-cc3e-4b83-8531-bc4bd6d665ac
title: 'COutputQueue：： m_hr 成員 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hr
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b786afa24f974d5eab7e13062105f26386da1c30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978685"
---
# <a name="coutputqueuem_hr-member"></a>COutputQueue：： m \_ hr 成員

**HRESULT** 值，指出物件是否會接受範例。 如果值為 S \_ OK，則物件會接受範例。 否則，它會拒絕範例。

## <a name="syntax"></a>語法


```C++
HRESULT m_hr;
```



## <a name="remarks"></a>備註

此成員變數用來協調執行緒之間的活動。 如果下游輸入 pin 拒絕範例，或物件開始排清，此值會設為 \_ FALSE 或錯誤碼。 在排清完成之前，或在呼叫 [**COutputQueue：： Reset**](coutputqueue-reset.md) 方法之前，物件將不會提供任何更多的範例。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Outputq (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COutputQueue 類別**](coutputqueue.md)
</dt> </dl>

 

 




