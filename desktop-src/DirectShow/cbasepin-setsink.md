---
description: SetSink 方法會設定外部品質管制員。 這個方法會實 IQualityControl：： SetSink 方法。
ms.assetid: 714e6839-954e-4231-824d-72a45f270f59
title: 'CBasePin. SetSink 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetSink
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4237e342f8f49059cab017b17a1f116ca6e2da67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983013"
---
# <a name="cbasepinsetsink-method"></a>CBasePin. SetSink 方法

`SetSink`方法會設定外部品質管制員。 這個方法會實 [**IQualityControl：： SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT SetSink(
   IQualityControl *piqc
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*piqc* 
</dt> <dd>

品質管制員 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

呼叫這個方法，將品質控制訊息重新導向至外部品質管制員。 如需詳細資訊，請參閱 [品質控制管理](quality-control-management.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




