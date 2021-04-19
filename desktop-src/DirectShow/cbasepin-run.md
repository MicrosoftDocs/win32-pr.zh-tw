---
description: Run 方法會通知釘選篩選現在正在執行。
ms.assetid: 74aafc89-2d3c-4259-a5b7-d4fb7628f539
title: 'CBasePin： Run 方法 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35d66f6d504a96c1146bc15285762d83faa6de3b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984315"
---
# <a name="cbasepinrun-method"></a>CBasePin 方法

`Run`方法會通知釘選篩選現在正在執行。

## <a name="syntax"></a>語法


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*tStart* 
</dt> <dd>

傳遞至篩選器 [**IMediaFilter：： Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) 方法的開始時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

當篩選從暫停變成執行中時， [**CBaseFilter**](cbasefilter.md) 類別會在所有篩選器的釘選上呼叫這個方法。

這個方法不會在基類中執行任何動作。 衍生類別可以覆寫這個方法。 例如，pin 可能會啟動可傳遞範例的背景工作執行緒。

除非這個成員函式傳回，否則篩選圖形管理員的內部狀態不會更新，因此請勿從此方法測試狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




