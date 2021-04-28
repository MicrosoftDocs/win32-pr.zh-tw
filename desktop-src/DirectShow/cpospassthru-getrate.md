---
description: CPosPassThru. GetRate 方法-GetRate 方法會捕獲播放速率。 這個方法會實 IMediaSeeking：： GetRate 方法。
ms.assetid: 19de3ea3-280e-4320-9cce-2c29801bd84b
title: 'CPosPassThru. GetRate 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 997323ca2089a0b381b85c3730cb364d0883b1bf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085556"
---
# <a name="cpospassthrugetrate-method"></a>CPosPassThru. GetRate 方法

`GetRate`方法會捕獲播放速率。 這個方法會實 [**IMediaSeeking：： GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT GetRate(
   double *pdRate
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pdRate* 
</dt> <dd>

接收播放速率之變數的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

從連接的 pin 傳回 **HRESULT** 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPosPassThru 類別**](cpospassthru.md)
</dt> </dl>

 

 




