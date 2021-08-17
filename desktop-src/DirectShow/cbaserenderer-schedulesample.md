---
description: ScheduleSample 方法會排定轉譯的範例。
ms.assetid: 08c218d1-6d0a-4c66-bbde-a39e5d31561c
title: 'CBaseRenderer. ScheduleSample 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ScheduleSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 88e728b90078ab11a6215dad60a88b819b2c513071637e2aa5c6b6ed7226189b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157590"
---
# <a name="cbaserendererschedulesample-method"></a>CBaseRenderer. ScheduleSample 方法

方法會排定轉譯的 `ScheduleSample` 範例。

## <a name="syntax"></a>語法


```C++
virtual BOOL ScheduleSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMediaSample* 
</dt> <dd>

範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果已排程範例，則傳回 **TRUE** ; 如果已卸載樣本，則傳回 **FALSE** 。

## <a name="remarks"></a>備註

這個方法會先判斷是否應該立即轉譯範例、在未來轉譯或卸載範例。  (這麼做，它會呼叫 [**CBaseRenderer：： GetSampleTimes**](cbaserenderer-getsampletimes.md) 方法。 ) 如果應該立即轉譯範例，則方法會表示 [**CBaseRenderer：： m \_ RenderEvent**](cbaserenderer-m-renderevent.md) 事件。 如果未來應轉譯此範例，則方法會呼叫 [**IReferenceClock：： AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) 方法來進行排程。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




